---
title: EAP \_ CRED \_ RESP (Eaptypes.h)
description: Almacena las credenciales de seguridad de EAP dentro de una estructura DE MATRIZ DE CAMPOS DE ENTRADA DE CONFIGURACIÓN \_ \_ DE \_ \_ EAP. | EAP \_ CRED \_ RESP (Eaptypes.h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b9bda55ed1b4aee9a9847740b25d46418c6ec3544dfdd6ba71b2c282042b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904642"
---
# <a name="eap_cred_resp"></a>EAP \_ CRED \_ RESP

La **estructura \_ \_ RESP de EAP CRED** almacena las credenciales de seguridad de EAP dentro de una estructura DE [**MATRIZ DE CAMPOS DE ENTRADA DE CONFIGURACIÓN \_ \_ \_ \_ DE EAP.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**EAP \_ CRED \_ RESP**
</dt> <dd>

La estructura **\_ \_ RESP** de EAP CRED almacena las credenciales de seguridad eap antiguas y nuevas a las que apunta el parámetro *pbUiData* de la estructura DE DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA de EAP cuando el parámetro *dwDataType* del tipo de datos de la interfaz de usuario interactiva de EAP especifica un tipo de respuesta de credencial. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ \_ RESP de EAP CRED** se usa para admitir el inicio de sesión único (SSO).

La **estructura \_ DE \_ RESP de EAP CRED** es idéntica a la estructura DE [**REQ de EAP \_ CRED. \_**](eap-cred-req.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras suplicantes de EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**SOLICITUD \_ DE EXPIRACIÓN CRED \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**DATOS DE \_ LA INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

