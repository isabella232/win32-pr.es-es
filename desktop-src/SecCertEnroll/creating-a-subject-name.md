---
description: Puede usar la interfaz IX500DistinguishedName para crear un nombre de sujeto a partir de una cadena de nombre distintivo.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Crear un nombre de sujeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a7350268c4b7fe5f0d6bde0630bfa7556bc8dd6085e11261456299b725dd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670215"
---
# <a name="creating-a-subject-name"></a>Crear un nombre de sujeto

Puede usar la interfaz [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) para crear un nombre de sujeto a partir de una cadena de nombre distintivo. La cadena consta de nombres distintivos relativos concatenados (RDN). La API de inscripción de certificados admite las siguientes claves RDN.

| Clave                               | OID                                             | Descripción                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | NOMBRE DE PAÍS \_ DEL OID \_ XCN \_<br/>              | Contiene un código de país o región ISO 3166 de dos letras.<br/>                                  |
| CN<br/>                     | NOMBRE COMÚN \_ DE OID \_ XCN \_<br/>               | Contiene un nombre común.<br/>                                                                 |
| E<br/> Correo electrónico<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | Contiene una dirección de correo electrónico.<br/>                                                              |
| DC<br/>                     | COMPONENTE DE DOMINIO \_ DE OID \_ de XCN \_<br/>          | Contiene una parte de un nombre de sistema de nombres de dominio (DNS).<br/>                                   |
| G<br/> GivenName<br/> | NOMBRE DADO \_ DEL OID \_ XCN \_<br/>                | Contiene la parte del nombre de una persona que no es un apellido.<br/>                             |
| I<br/>                      | INICIALES \_ DE OID \_ XCN<br/>                   | Contiene las iniciales de una persona.<br/>                                                           |
| L<br/>                      | NOMBRE DE LA LOCALIDAD \_ DEL OID \_ XCN \_<br/>             | Contiene el nombre de localidad que identifica una ciudad, un país u otra región geográfica.<br/> |
| O<br/>                      | NOMBRE DE LA \_ ORGANIZACIÓN DE OID \_ XCN \_<br/>         | Contiene el nombre de una organización.<br/>                                                   |
| OU<br/>                     | XCN \_ OID \_ ORGANIZATIONAL \_ UNIT \_ NAME<br/> | Contiene el nombre de una subdivisión de unidad dentro de una organización.<br/>                         |
| S<br/> ST<br/>        | XCN \_ OID \_ STATE \_ OR \_ PROVINCE \_ NAME<br/>  | Contiene el nombre completo de un estado o provincia.<br/>                                          |
| STREET<br/>                 | DIRECCIÓN POSTAL \_ DEL OID \_ XCN \_<br/>            | Contiene la dirección física.<br/>                                                          |
| SN<br/>                     | NOMBRE DEL SUR \_ del OID \_ XCN \_<br/>                  | Contiene el nombre de familia de una persona.<br/>                                                   |
| T<br/> TITLE<br/>     | TÍTULO DEL \_ OID de XCN \_<br/>                      | Contiene el título de una persona de la organización.<br/>                                     |



 

Al inicializar un objeto [**IX500DistinguishedName,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) puede identificar el formato del nombre distintivo especificando un valor del tipo de enumeración [**X500NameFlags.**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) Por ejemplo, suponga que el nombre distintivo del sujeto consta de los siguientes RDN:<dl> CN=Administrador  
CN=Usuarios  
DC=jdomcsc  
DC=nttest  
DC=microsoft  
DC=com  
</dl>

Si concatena estos RDN en la siguiente cadena de nombre distintivo delimitado por comas, puede especificar el valor **XCN \_ CERT NAME STR COMMA \_ \_ \_ \_ FLAG** al inicializar un objeto [**IX500DistinguishedName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de un nombre de sujeto](encoding-a-subject-name.md)
</dt> <dt>

[Nombres de sujeto](subject-names.md)
</dt> </dl>

 

 




