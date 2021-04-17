---
title: EAP \_ CRED \_ Resp (Eaptypes. h)
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ . | EAP \_ CRED \_ Resp (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717455"
---
# <a name="eap_cred_resp"></a>respuesta de cred de EAP \_ \_

La estructura de la **\_ \_ resp de EAP de EAP** almacena las credenciales de seguridad de EAP en una estructura de matriz de [**campos de entrada de configuración de EAP \_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**respuesta de cred de EAP \_ \_**
</dt> <dd>

La estructura de la **\_ \_ resp de EAP de EAP** almacena las credenciales de seguridad de EAP antiguas y nuevas a las que apunta el parámetro *pbUiData* de la estructura de datos de [**interfaz de \_ \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *DwDataType* del tipo de [**datos de interfaz de \_ \_ usuario \_ \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de respuesta de credencial.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ resp de EAP** se usa para admitir el inicio de sesión único (SSO).

La estructura de **\_ \_ resp de EAP** es idéntica a la estructura de REQ de la [**\_ \_ solicitud EAP**](eap-cred-req.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de suplicante de EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**\_solicitud de credenciales de EAP \_**](eap-cred-req.md)
</dt> <dt>

[**\_solicitud de \_ expiración de credenciales de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**respuesta \_ de \_ expiración de credenciales de EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

