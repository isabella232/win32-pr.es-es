---
title: EAP \_ CRED \_ Logon \_ Resp (Eaptypes. h)
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ . | EAP \_ CRED \_ Logon \_ Resp (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698120"
---
# <a name="eap_cred_logon_resp"></a>EAP de inicio de sesión de la \_ \_ \_ resp

La estructura de **\_ resp de inicio de \_ \_ sesión de EAP** almacena las credenciales de seguridad de EAP en una estructura de [**\_ \_ \_ \_ matriz de campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**EAP de inicio de sesión de la \_ \_ \_ resp**
</dt> <dd>

La estructura de **resp de \_ Inicio de \_ sesión \_ de EAP** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura de datos de [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *dwDataType* del [**\_ \_ \_ \_ tipo de datos Interactive UI de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credencial Los campos de entrada de esta estructura serán los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ de CRED \_ Logon \_ resp** se usa en la solicitud de credenciales inicial y [**EAP \_ CRED \_ resp**](eap-cred-resp.md) se usa en la solicitud de reintento de credencial durante una autenticación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de uso de **\_ credenciales de \_ Inicio de sesión \_ de EAP** se usa para admitir el inicio de sesión único (SSO).

La estructura de **\_ resp de inicio de \_ \_ sesión de EAP** es idéntica a la estructura [**\_ \_ \_ req del inicio de sesión de EAP**](eap-cred-logon-req.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**\_solicitud de \_ Inicio de sesión de recred de EAP \_**](eap-cred-logon-req.md)
</dt> <dt>

[**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





