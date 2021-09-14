---
title: Constantes de error de EAP \_ CERT (Eaphosterror.h)
description: Defina errores relacionados con certificados comunes a todas las tecnologías de API de EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168445"
---
# <a name="eap_cert-error-constants"></a>Constantes de error de EAP \_ CERT

Estas constantes definen errores relacionados con certificados comunes a todas las tecnologías de API de EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Define el límite de los informes de errores; cualquier error de certificado se producirá entre **\_ EAP CERT \_ \_ FIRST** y **\_ EAP CERT \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Define el límite de los informes de errores; cualquier error de certificado se producirá entre **\_ EAP CERT \_ \_ FIRST** y **\_ EAP CERT \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_NO SE \_ ENCONTRÓ EL CERTIFICADO DE \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



No se encontró ningún certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_CERTIFICADO EAP \_ \_ NO VÁLIDO**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



El certificado de usuario no es válido.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP \_ CERT EXPIRED (CERTIFICADO EAP \_ EXPIRADO)**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



El certificado de usuario ha expirado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_CERTIFICADO \_ EAP \_ REVOCADO**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Se revocó el certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Hay un error relacionado con el certificado desconocido.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_CERTIFICADO \_ EAP \_ RECHAZADO**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Se rechazó el certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_SE REQUIERE \_ EL NOMBRE DEL CERTIFICADO \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



El certificado de usuario requiere un nombre.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ GENERAL \_ FIRST**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Define el límite de los informes de errores; cualquier error general de EAP se producirá entre **\_ EAP GENERAL \_ \_ FIRST** y **\_ EAP GENERAL \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ GENERAL \_ LAST**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Define el límite de los informes de errores; cualquier error general de EAP se producirá entre **\_ EAP GENERAL \_ \_ FIRST** y **\_ EAP GENERAL \_ \_ LAST**.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Eaphosterror.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes comunes de EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

 

 





