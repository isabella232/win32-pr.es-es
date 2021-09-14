---
description: Representa el control de inscripción de tarjeta inteligente.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170945"
---
# <a name="iscrdenr-interface"></a>Interfaz ISCrdEnr

La **interfaz ISCrdEnr** representa el control de inscripción de tarjeta inteligente. Es principalmente de interés para los desarrolladores que no usan Automation. Para programar en Visual Basic u otro lenguaje de Automation, vea el [**objeto CEnroll.**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))

## <a name="members"></a>Members

La **interfaz ISCrdEnr** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCrdEnr** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ISCrdEnr** tiene estos métodos.



| Método                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inscribirse**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Solicita un certificado en nombre del usuario y almacena el [*certificado*](../secgloss/c-gly.md) resultante en la tarjeta inteligente [*del usuario.*](../secgloss/s-gly.md)<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Enumera los nombres de las entidades de [*certificación*](../secgloss/c-gly.md) (CA) para un nombre de plantilla de certificado determinado.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Enumera los nombres de las plantillas de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Enumera el nombre de los proveedores de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) disponibles.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Devuelve el número de CA que están dispuestos a emitir un certificado en función de la plantilla de certificado especificada.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Recupera el nombre de la entidad de certificación especificada para una plantilla de certificado determinada.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Recupera el número de plantillas de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Recupera el nombre de la plantilla de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Determine si una plantilla de certificado contiene el uso de clave szOID \_ PKIX \_ KP EMAIL \_ \_ PROTECTION. Si este uso de clave forma parte de la plantilla de certificado, la plantilla de certificado admite operaciones de extensiones de correo de Internet (S/MIME) [*seguras*](../secgloss/s-gly.md) o multipropósito.<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Recupera el nombre del certificado resultante de una llamada correcta anterior a [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Este método también se puede usar para mostrar el certificado en un cuadro de diálogo.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Recupera el nombre del firmantes del certificado de firma. Este método también se puede usar para mostrar el certificado en un cuadro de diálogo. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Recupera el nombre del usuario en cuyo nombre está prevista la inscripción del certificado.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Borra el nombre de usuario del control de tarjeta inteligente.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Muestra un **cuadro de diálogo Seleccionar** certificado que permite seleccionar un certificado de firma (también conocido como certificado del *agente* de inscripción).<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Muestra un **cuadro de diálogo Seleccionar** usuario que permite seleccionar un nombre de usuario. El nombre de usuario se aplica al usuario en cuyo nombre está prevista la inscripción del certificado.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Especifica el nombre de la entidad de certificación.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Especifica el nombre de la plantilla de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Especifica un certificado de firma (también conocido como certificado *del agente de inscripción).*<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Especifica el nombre del usuario en cuyo nombre está prevista la inscripción del certificado.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **interfaz ISCrdEnr** tiene estas propiedades.



| Propiedad                                         | Tipo de acceso           | Descripción                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Solo lectura<br/>  | Especifica el número de CSP. Esta propiedad es de solo lectura.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lectura y escritura<br/> | Nombre del CSP. Esta propiedad es de lectura y escritura. <br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
