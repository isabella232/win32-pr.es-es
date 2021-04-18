---
title: '\_Constantes de error de certificado EAP (Eaphosterror. h)'
description: Defina los errores relacionados con los certificados comunes a todas las tecnologías de API de EAPHost.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533903"
---
# <a name="eap_cert-error-constants"></a>\_Constantes de error de certificado EAP

Estas constantes definen errores relacionados con los certificados comunes a todas las tecnologías de API de EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificado EAP \_ primero**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Define el límite de los informes de errores; en **\_ \_ \_ último** lugar, se producirá un error de certificado entre el certificado **\_ EAP \_ \_** y el certificado EAP.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_último certificado \_ EAP**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Define el límite de los informes de errores; en **\_ \_ \_ último** lugar, se producirá un error de certificado entre el certificado **\_ EAP \_ \_** y el certificado EAP.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_ \_ no \_ se encontró el certificado EAP**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



No se encontró ningún certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificado EAP \_ no válido**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



El certificado de usuario no es válido.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificado EAP \_ expirado**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



El certificado de usuario ha expirado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificado EAP \_ revocado**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Se revocó el certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_error de \_ otro \_ certificado EAP**
</dt> <dd> <dl> <dt>

0X5
</dt> <dt>



Error desconocido relacionado con el certificado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificado EAP \_ rechazado**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Se rechazó el certificado de usuario.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_se \_ \_ requiere el nombre de certificado EAP \_**
</dt> <dd> <dl> <dt>

0X7
</dt> <dt>



El certificado de usuario requiere un nombre.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ General \_ primero**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Define el límite de los informes de errores; cualquier error de EAP general se producirá entre **\_ EAP \_ General \_ primero** y **\_ EAP \_ General en \_ último** lugar.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_último EAP general \_**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Define el límite de los informes de errores; cualquier error de EAP general se producirá entre **\_ EAP \_ General \_ primero** y **\_ EAP \_ General en \_ último** lugar.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de EAPHost comunes](common-eap-host-error-constants.md)
</dt> </dl>

 

 





