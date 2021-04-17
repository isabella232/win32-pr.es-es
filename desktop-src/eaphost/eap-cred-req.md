---
title: '\_Solicitud de credenciales de EAP \_ (Eaptypes. h)'
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ . | \_Solicitud de credenciales de EAP \_ (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698119"
---
# <a name="eap_cred_req"></a>\_solicitud de credenciales de EAP \_

La **estructura \_ \_ req req de EAP** almacena las credenciales de seguridad de EAP dentro de una estructura de matriz de [**campos de entrada de configuración de EAP \_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**\_solicitud de credenciales de EAP \_**
</dt> <dd>

La **estructura \_ \_ req req de EAP** almacena las credenciales de seguridad de EAP antiguas y nuevas a las que apunta el parámetro *pbUiData* de la estructura de datos de [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *DwDataType* del tipo de [**datos de interfaz de \_ usuario interactiva \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credenciales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ solicitud de credenciales de EAP** se usa para admitir el inicio de sesión único (SSO).

La estructura de REQ de la **\_ \_ solicitud EAP** es idéntica a la estructura de [**\_ \_ resp de EAP**](eap-cred-resp.md) .

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

[**respuesta de cred de EAP \_ \_**](eap-cred-resp.md)
</dt> <dt>

[**\_solicitud de \_ expiración de credenciales de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**respuesta \_ de \_ expiración de credenciales de EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO y PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

