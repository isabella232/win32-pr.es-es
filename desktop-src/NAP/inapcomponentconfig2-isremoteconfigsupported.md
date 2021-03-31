---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para indicar si se admite la configuración remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Método IsRemoteConfigSupported NAP
- Método IsRemoteConfigSupported NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método IsRemoteConfigSupported
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
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996187"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2:: IsRemoteConfigSupported (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **IsRemoteConfigSupported** para indicar si se admite la configuración remota.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isSupported* \[ enuncia\]
</dt> <dd>

Un puntero a un valor BOOLEANO que se establece en **true** si el componente admite la configuración remota y **false** en caso contrario.

</dd> <dt>

*remoteConfigType* \[ enuncia\]
</dt> <dd>

Indica el tipo de configuración remota admitida mediante el valor de la enumeración [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :



| Value                                                                                                 | Significado                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | Se implementa [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) .<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | Se implementa [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) . Se puede llamar a [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) y [**INapComponentConfig:: SetConfig**](inapcomponentconfig-setconfig.md) de forma remota mediante DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.

## <a name="remarks"></a>Observaciones

Si no se implementan [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ni [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) , no es posible la configuración remota del SHV.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





