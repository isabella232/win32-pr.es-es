---
title: EAP \_ CRED \_ LOGON \_ RESP (Eaptypes.h)
description: Almacena las credenciales de seguridad de EAP dentro de una estructura \_ EAP CONFIG INPUT FIELD \_ \_ \_ ARRAY. | EAP \_ CRED \_ LOGON \_ RESP (Eaptypes.h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36327de109fc22d6114b18d785e678c68d3d9f86f69bdb4587eff917743d1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904841"
---
# <a name="eap_cred_logon_resp"></a>EAP \_ CRED \_ LOGON \_ RESP

La **estructura \_ \_ \_ RESP EAP CRED LOGON** almacena las credenciales de seguridad de EAP dentro de una estructura DE MATRIZ DE CAMPO DE ENTRADA DE CONFIGURACIÓN [**\_ \_ \_ \_ DE EAP.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**EAP \_ CRED \_ LOGON \_ RESP**
</dt> <dd>

La estructura **\_ \_ \_ RESP EAP CRED LOGON** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura DE DATOS de la interfaz de usuario interactiva de EAP cuando el parámetro *dwDataType* de [**EAP INTERACTIVE UI DATA \_ \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credenciales. [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) Los campos de entrada de esta estructura serán los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ CRED \_ LOGON \_ RESP** se usa en la solicitud de credencial inicial y [**EAP \_ CRED \_ RESP**](eap-cred-resp.md) se usa en la solicitud de reintento de credenciales durante una autenticación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ \_ \_ RESP EAP CRED LOGON** se usa para admitir el inicio de sesión único (SSO).

La **estructura \_ \_ \_ RESP DE EAP CRED LOGON** es idéntica a la estructura [**REQ DE EAP \_ CRED \_ LOGON. \_**](eap-cred-logon-req.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**MATRIZ DE \_ CAMPOS DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP \_ CRED \_ LOGON \_ REQ**](eap-cred-logon-req.md)
</dt> <dt>

[**DATOS DE \_ LA INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**TIPO DE \_ DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





