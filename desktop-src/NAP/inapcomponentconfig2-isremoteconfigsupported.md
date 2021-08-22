---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) para indicar si se admite la configuración remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Método NAP isRemoteConfigSupported
- Método NAP de IsRemoteConfigSupported, interfaz INapComponentConfig2
- INapComponentConfig2 interface NAP , IsRemoteConfigSupported method
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621772"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2::IsRemoteConfigSupported (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **IsRemoteConfigSupported** para indicar si se admite la configuración remota.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isSupported* \[ out\]
</dt> <dd>

Puntero a un BOOL que se establece en **TRUE** si el componente admite la configuración remota y **FALSE** si no lo hace.

</dd> <dt>

*remoteConfigType* \[ out\]
</dt> <dd>

Indica el tipo de configuración remota admitida mediante el valor de la [**enumeración RemoteConfigurationType:**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype)



| Value                                                                                                 | Significado                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**Se implementa InvokeUIForMachine.**](inapcomponentconfig2-invokeuiformachine.md)<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**Se implementa InvokeUIFromConfigBlob.**](inapcomponentconfig2-invokeuifromconfigblob.md) [**Se puede llamar a INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) [**e INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) de forma remota mediante DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o uno de los códigos de error Windows estándar.

## <a name="remarks"></a>Observaciones

Si no [**se implementan InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ni [**InvokeUIFromConfigBlob,**](inapcomponentconfig2-invokeuifromconfigblob.md) la configuración remota de shv no es posible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





