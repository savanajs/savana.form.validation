# Savana form validation
Use:
     
    $savana(window).onload(function(e){

        var $formValidations = $savana("form#form-exemplo").formValidations(); // Load plugin
            $formValidations.masks(); // Show masks

            $savana("form#form-exemplo").on("submit", function(e){        
                  var form = $formValidations.validations(); // Validations
                  if(form.hasError){ // Case errors
                     savana.eventStop(e); // Stop script
                  }else{
                     // submit ok
                  }
                }   
            });

    });

  

##All params:

  

     
     {
            requeredClassName: 'ht-required',
            validateEmailClassName: 'ht-valid-email',
            validateCPFClassName: 'ht-valid-cpf',
            validateLastanameClassName: 'ht-valid-name-and-lastname',
            validateNumberClassName: 'ht-valid-number',
            validateLetterClassName: 'ht-valid-letter',
            maskCEPClassName: 'ht-mask-cep',
            maskCPFClassName: 'ht-mask-cpf',
            maskCNPJClassName: 'ht-mask-cnpj',
            maskPhoneClassName: 'ht-mask-phone',
            maskRGClassName: 'ht-mask-rg',
            maskDataNascClassName: 'ht-mask-date',
            maskNumberClassName: 'ht-mask-number',
            maskLetterClassName: 'ht-mask-letters',
            msgRequered: "O campo <b>'{&}'</b> é de tipo obrigatório!",
            msgEmailValidate: "O campo <b>'{&}'</b> está no formato inválido!",
            msgCPFValidate: "O campo <b>'{&}'</b> está no formato inválido!",
            msgNameAndLastnameValidate: "O campo <b>'{&}'</b> está inválido, digite seu sobrenome!",
            msgNumberValidate: "O campo <b>'{&}'</b> está inválido, digite apenas numeros!",
            msgLetterValidate: "O campo <b>'{&}'</b> está inválido, digite apenas letras!",
            msgForUserOfInputRequered: "<p><span>*</span> Campos obrigatórios!</p>",
            placeholderMaskCEP: "Ex: 99999-999",
            placeholderMaskNumber: "Ex: 99999...",
            placeholderMaskDate: "Ex: 31/12/1980",
            placeholderMaskCPF: "Ex: 999.999.999-99",
            placeholderMaskCNPJ: "Ex: 99.999.999/9999-99",
            placeholderMaskRG: "Ex: 99.999.999-9",
            placeholderMaskPhone: "Ex: (11) 9999-99999"
        };

  

##HTML:
Enter the attribute is the label to identify the field in the error message 
Use the classes for validation and masks 

##Classes
```
ht-required: Required field
ht-valid-email: Email validation
ht-valid-cpf: CPF validation
ht-valid-name-and-lastname: Name validation and surname
ht-valid-letter: Validation letters
ht-valid-number: Validation numbers
ht-mask-cep: CEP mask
ht-mask-cpf: CPF mask
ht-mask-cnpj: CNPJ mask
ht-mask-phone: Phone mask
ht-mask-rg: RG mask
ht-mask-date: Date mask
ht-mask-number: Number mask
ht-mask-letters: Letters mask
```
  
```
<form id="form-exemplo" action="Script_do_Formulario.php" method="post">
<!-- DADOS PESSOAIS-->
<fieldset>
 <legend>Dados Pessoais</legend>
 <table cellspacing="10">
  <tr>
   <td>
    <label for="email">Email: </label>
   </td>
   <td align="left">
    <input type="text" name="email" id="email" class="">
   </td>
   <td>
    <label for="nome">Nome: </label>
   </td>
   <td align="left">
    <input type="text" name="nome" id="nome" class="ht-required ht-valid-name-and-lastname 
    ht-valid-letter ht-mask-letters">
   </td>
  </tr>
 </table>
</fieldset>
<br />
<input type="submit">
<input type="reset" value="Limpar">
</form>
```

