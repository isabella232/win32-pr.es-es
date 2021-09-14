---
title: EAP \_ CRED \_ REQ (Eaptypes.h)
description: Almacena las credenciales de seguridad de EAP dentro de una estructura DE MATRIZ DE CAMPOS DE ENTRADA DE CONFIGURACIÓN \_ \_ DE \_ \_ EAP. | EAP \_ CRED \_ REQ (Eaptypes.h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253017"
---
# <a name="eap_cred_req"></a>EAP \_ CRED \_ REQ

La **estructura \_ DE \_ REQ de EAP CRED** almacena las credenciales de seguridad de EAP dentro de una estructura DE [**MATRIZ DE CAMPOS DE ENTRADA DE CONFIGURACIÓN \_ \_ \_ \_ DE EAP.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**EAP \_ CRED \_ REQ**
</dt> <dd>

La estructura **\_ \_ REQ de EAP CRED** almacena las credenciales de seguridad de EAP antiguas y nuevas a las que apunta el parámetro *pbUiData* de la estructura DE DATOS de la interfaz de usuario interactiva de EAP cuando el parámetro *dwDataType* del tipo de datos de la interfaz de usuario interactiva de EAP especifica un tipo de solicitud de credenciales. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) [**\_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura \_ DE \_ REQ de EAP CRED** se usa para admitir el inicio de sesión único (SSO).

La **estructura \_ DE \_ REQ de EAP CRED** es idéntica a la estructura DE [**\_ \_ RESP de EAP CRED.**](eap-cred-resp.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras suplicantes de EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ CRED \_ RESP**](eap-cred-resp.md)
</dt> <dt>

[**SOLICITUD \_ DE EXPIRACIÓN CRED \_ \_ DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**DATOS DE LA \_ INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

