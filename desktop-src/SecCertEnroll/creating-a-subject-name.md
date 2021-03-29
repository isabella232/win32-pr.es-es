---
description: Puede usar la interfaz IX500DistinguishedName para crear un nombre de sujeto a partir de una cadena de nombre distintivo.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Crear un nombre de sujeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540155"
---
# <a name="creating-a-subject-name"></a>Crear un nombre de sujeto

Puede usar la interfaz [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) para crear un nombre de sujeto a partir de una cadena de nombre distintivo. La cadena consta de nombres distintivos relativos (RDN) concatenados. Las siguientes claves RDN son compatibles con la API de inscripción de certificados.

| Clave                               | OID                                             | Descripción                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | XCN \_ \_ nombre del país OID \_<br/>              | Contiene un código de país o región ISO 3166 de dos letras.<br/>                                  |
| CN<br/>                     | \_ \_ nombre común de OID de XCN \_<br/>               | Contiene un nombre común.<br/>                                                                 |
| E<br/> Correo electrónico<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | Contiene una dirección de correo electrónico.<br/>                                                              |
| DC<br/>                     | \_componente de \_ dominio \_ OID de XCN<br/>          | Contiene una parte de un nombre DNS (sistema de nombres de dominio).<br/>                                   |
| G<br/> GivenName<br/> | \_nombre XCN OID \_ proporcionado \_<br/>                | Contiene la parte del nombre de una persona que no es un apellido.<br/>                             |
| I<br/>                      | iniciales de XCN \_ OID \_<br/>                   | Contiene las iniciales de una persona.<br/>                                                           |
| L<br/>                      | XCN \_ nombre de la localidad del OID \_ \_<br/>             | Contiene el nombre de la localidad que identifica una ciudad, un país u otra región geográfica.<br/> |
| O<br/>                      | XCN \_ nombre de la \_ organización OID \_<br/>         | Contiene el nombre de una organización.<br/>                                                   |
| OU<br/>                     | \_nombre de \_ \_ unidad organizativa XCN OID \_<br/> | Contiene el nombre de una subdivisión de unidad dentro de una organización.<br/>                         |
| S<br/> ST<br/>        | XCN \_ \_ \_ nombre de estado o \_ provincia de \_ OID<br/>  | Contiene el nombre completo de un estado o provincia.<br/>                                          |
| STREET<br/>                 | \_Dirección XCN \_ OID \_<br/>            | Contiene la dirección física.<br/>                                                          |
| SN<br/>                     | nombre de XCN \_ OID \_ sur \_<br/>                  | Contiene el nombre de familia de una persona.<br/>                                                   |
| T<br/> TITLE<br/>     | \_título XCN OID \_<br/>                      | Contiene el título de una persona de la organización.<br/>                                     |



 

Al inicializar un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , puede identificar el formato del nombre distintivo especificando un valor del tipo de enumeración [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) . Por ejemplo, supongamos que el nombre distintivo del sujeto consta del siguiente RDN:<dl> CN = administrador  
CN = usuarios  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>

Si concatena estos RDN en la siguiente cadena de nombres distintivos delimitados por comas, puede especificar el valor de **\_ \_ \_ \_ \_ marcador de coma Str del nombre de certificado XCN** al inicializar un objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificar un nombre de sujeto](encoding-a-subject-name.md)
</dt> <dt>

[Nombres de sujeto](subject-names.md)
</dt> </dl>

 

 




