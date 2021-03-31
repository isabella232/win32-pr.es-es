---
title: Propiedad AuthenticationServiceClass de IMsRdpClientAdvancedSettings6
description: Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AuthenticationServiceClass
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
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802288"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a>IMsRdpClientAdvancedSettings6:: AuthenticationServiceClass (propiedad)

Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nombre de la entidad de seguridad de servicio que se va a usar.

## <a name="remarks"></a>Observaciones

Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.

Los nombres principales de servicio (SPN) están asociados a la entidad de seguridad (usuarios o grupos) en cuyo contexto de seguridad se ejecuta el servicio. Los SPN se usan para admitir la autenticación mutua entre una aplicación cliente y un servicio.

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

 

 





