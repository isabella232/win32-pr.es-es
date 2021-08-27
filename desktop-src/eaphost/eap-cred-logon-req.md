---
title: EAP \_ CRED \_ LOGON \_ REQ (Eaptypes.h)
description: Almacena las credenciales de seguridad de EAP dentro de una estructura \_ EAP CONFIG INPUT FIELD \_ \_ \_ ARRAY.
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719abbed6c16deb6d3bfd61811f3f24253181364fe89f5823ee682bafef001e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785628"
---
# <a name="eap_cred_logon_req"></a>EAP \_ CRED \_ LOGON \_ REQ

La **estructura \_ \_ \_ REQ DE EAP CRED LOGON** almacena las credenciales de seguridad de EAP dentro de una estructura DE [**MATRIZ DE CAMPO DE ENTRADA DE CONFIGURACIÓN \_ \_ \_ \_ DE EAP.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**EAP \_ CRED \_ LOGON \_ REQ**
</dt> <dd>

La estructura **\_ \_ \_ REQ EAP CRED LOGON** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura DE DATOS de la interfaz de usuario interactiva de EAP cuando el parámetro *dwDataType* de [**EAP INTERACTIVE UI DATA \_ \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credenciales. [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Los campos de entrada de esta estructura son los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ CRED \_ LOGON \_ REQ se** usa en la solicitud de credencial inicial y EAP [**\_ CRED \_ REQ**](eap-cred-req.md) se usa en la solicitud de reintento de credenciales durante una autenticación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ \_ \_ REQ DE EAP CRED LOGON** se usa para admitir el inicio de sesión único (SSO).

La **estructura \_ \_ \_ REQ DE EAP CRED LOGON** es idéntica a la estructura [**\_ \_ \_ RESP DE EAP CRED LOGON.**](eap-cred-logon-resp.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MATRIZ DE \_ CAMPOS DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**DATOS DE \_ LA INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**TIPO DE \_ DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





