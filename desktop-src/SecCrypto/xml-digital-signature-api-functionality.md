---
description: CryptXML proporciona un conjunto de bajo nivel de API que permiten a las aplicaciones crear y comprobar firmas con doble cifrado, envoltura y desconectadas. Puede usar CryptXML para crear y comprobar el contenido almacenado en los elementos del objeto Signature, incluidos los manifiestos.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funcionalidad de la API de firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667529"
---
# <a name="xml-digital-signature-api-functionality"></a>Funcionalidad de la API de firma digital XML

CryptXML proporciona un conjunto de bajo nivel de API que permiten a las aplicaciones crear y comprobar firmas con doble cifrado, envoltura y desconectadas. Puede usar CryptXML para crear y comprobar el contenido almacenado en los elementos del objeto Signature, incluidos los manifiestos. Se puede usar una clave pública o privada, una clave compartida o un certificado [*X. 509*](../secgloss/x-gly.md) o una cadena de certificados para firmar y comprobar la [*firma digital*](../secgloss/d-gly.md)XML.

Las aplicaciones que usan CryptXML para comprobar las referencias externas (referencias destinadas a un documento o archivo externo fuera del contexto del documento) deben resolver los URI externos y recuperar los datos que se van a resumir.

Para obtener información sobre los algoritmos criptográficos admitidos por CryptXML, consulte [algoritmos criptográficos de la firma digital XML](xml-digital-signature-cryptographic-algorithms.md).

CryptXML proporciona compatibilidad con los algoritmos de canonización con los siguientes identificadores.



| Constante                                              | Valor de URI                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| wszURI \_ canonicalización de la canonización \_<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| wszURI \_ canonización \_ C14NC<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszURI \_ canonicalización \_ EXSLUSIVE \_ C14N<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszURI \_ canonicalización \_ EXSLUSIVE \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

CryptXML proporciona compatibilidad con la transformación de firma con doble cifrado.



| Constante                                       | Valor de URI                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| wszURI \_ xmlns \_ Transform \_ sobre<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

De forma predeterminada, CryptXML no admite las transformaciones XPath o XSLT. Si es necesario, las aplicaciones pueden implementar estas transformaciones en la parte superior de CryptXML.

 

 
