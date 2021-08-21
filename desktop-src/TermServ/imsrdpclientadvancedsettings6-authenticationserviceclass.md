---
title: Propiedad IMsRdpClientAdvancedSettings6 AuthenticationServiceClass
description: Especifica el nombre de entidad de seguridad de servicio (SPN) que se usará para la autenticación en el servidor.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad AuthenticationServiceClass
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8453c0aef1548303e653f1ba57c9f05550975d93706eae1b9d3f05ea0b611a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001373"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a>Propiedad IMsRdpClientAdvancedSettings6::AuthenticationServiceClass

Especifica el nombre de entidad de seguridad de servicio (SPN) que se usará para la autenticación en el servidor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nombre de entidad de seguridad de servicio que se usará.

## <a name="remarks"></a>Comentarios

Esta propiedad solo es compatible con Conexión a Escritorio remoto 6.1 y 7.0.

Los nombres de entidad de seguridad de servicio (SPN) están asociados a la entidad de seguridad (usuario o grupos) en cuyo contexto de seguridad se ejecuta el servicio. Los SPN se usan para admitir la autenticación mutua entre una aplicación cliente y un servicio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





