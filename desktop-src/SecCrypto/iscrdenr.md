---
description: Representa el control de inscripción de tarjetas inteligentes.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: Interfaz ISCrdEnr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 3c3c882020db8b25c587a8d95824b3c90232bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669888"
---
# <a name="iscrdenr-interface"></a>Interfaz ISCrdEnr

La interfaz **ISCrdEnr** representa el control de inscripción de tarjetas inteligentes. Es principalmente interesante para los desarrolladores que no usan automatización. Para programar en Visual Basic u otro lenguaje de automatización, vea el objeto [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) .

## <a name="members"></a>Miembros

La interfaz **ISCrdEnr** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCrdEnr** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ISCrdEnr** tiene estos métodos.



| Método                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Solicita un certificado en nombre del usuario y almacena el [*certificado*](../secgloss/c-gly.md) resultante en la [*tarjeta inteligente*](../secgloss/s-gly.md)del usuario.<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Enumera los nombres de las [*entidades de certificación*](../secgloss/c-gly.md) (CA) para un nombre de plantilla de certificado determinado.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Enumera los nombres de las plantillas de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Enumera el nombre de los proveedores de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) disponibles.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Devuelve el número de entidades de certificación que están dispuestos a emitir un certificado basado en la plantilla de certificado especificada.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Recupera el nombre de la entidad de certificación especificada para una plantilla de certificado determinada.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Recupera el número de plantillas de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Recupera el nombre de la plantilla de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Determinar si una plantilla de certificado contiene el \_ uso de la \_ clave de protección del correo electrónico szOID PKIX PK \_ \_ . Si el uso de esta clave forma parte de la plantilla de certificado, la plantilla de certificado admite operaciones de [*extensiones seguras multipropósito de correo Internet*](../secgloss/s-gly.md) (S/MIME).<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Recupera el nombre del certificado resultante de una llamada correcta anterior a [**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Recupera el nombre del firmante del certificado de firma. Este método también se puede utilizar para mostrar el certificado en un cuadro de diálogo. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Recupera el nombre del usuario en cuyo nombre está diseñada la inscripción de certificados.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetuser**](iscrdenr-resetuser.md)                                   | Borra el nombre de usuario del control de tarjeta inteligente.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Muestra un cuadro de diálogo **seleccionar certificado** que permite seleccionar un certificado de firma (también conocido como *certificado de agente de inscripción*).<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Muestra un cuadro de diálogo **Seleccionar usuario** que permite seleccionar un nombre de usuario. El nombre de usuario se aplica al usuario en cuyo nombre está diseñada la inscripción de certificado.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Especifica el nombre de la CA.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Especifica el nombre de la plantilla de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Especifica un certificado de firma (también conocido como *certificado de agente de inscripción*).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Especifica el nombre del usuario en cuyo nombre se ha diseñado la inscripción de certificados.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La interfaz **ISCrdEnr** tiene estas propiedades.



| Propiedad                                         | Tipo de acceso           | Descripción                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Solo lectura<br/>  | Especifica el número de CSP. Esta propiedad es de solo lectura.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lectura/escritura<br/> | Nombre del CSP. Esta propiedad es de lectura y escritura. <br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
