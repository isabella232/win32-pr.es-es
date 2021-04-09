---
title: '\_Solicitud de \_ Inicio de sesión \_ (Eaptypes. h) de EAP'
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079140"
---
# <a name="eap_cred_logon_req"></a>\_solicitud de \_ Inicio de sesión de recred de EAP \_

La estructura de **solicitudes de inicio de sesión de EAP \_ \_ \_ CRED** almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de [**\_ configuración \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**\_solicitud de \_ Inicio de sesión de recred de EAP \_**
</dt> <dd>

La estructura de solicitudes de **\_ Inicio de \_ sesión \_ de EAP CRED** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura de [**\_ datos de interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *dwDataType* del tipo de datos de [**\_ interfaz de usuario interactiva \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo Los campos de entrada de esta estructura son los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ de CRED \_ Logon \_ req** se usa en la solicitud de credenciales inicial y se usa la solicitud de reintento de [**EAP \_ \_**](eap-cred-req.md) en la solicitud de reintento de credencial durante una autenticación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura \_ \_ \_ req de inicio de sesión de EAP** se usa para admitir el inicio de sesión único (SSO).

La estructura de **\_ req de inicio de \_ sesión \_ de EAP** es idéntica a la estructura de [**\_ \_ \_ resp de inicio**](eap-cred-logon-resp.md) de sesión de EAP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**\_solicitud de credenciales de EAP \_**](eap-cred-req.md)
</dt> <dt>

[**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





