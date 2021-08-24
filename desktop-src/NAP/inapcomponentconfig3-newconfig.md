---
title: Método INapComponentConfig3 NewConfig (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Nap del método NewConfig
- Método Nap de NewConfig, interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff87f55218d8c84b1cb95a75e1801783e57b17288c36057323589ab44a47d3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891345"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3::NewConfig (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los **validadores de** estado del sistema (SHV) implementan el método NewConfig para proporcionar una manera de crear datos de configuración para un identificador de configuración específico. Cuando se llama a esta función, una SHV debe asignar nuevos datos de configuración y rellenarlos con una copia de los datos de configuración predeterminados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* 
</dt> <dd>

Valor que representa la configuración. *ConfigID* está asignado por el servicio servidor de directivas de red (NPS) y es único dentro de la SHV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error según el resultado de esta operación.



| Código devuelto                                                                                                 | Descripción                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* es 0 (un valor reservado para la configuración predeterminada).<br/>                  |
| <dl> <dt>**EXISTÍA \_ LA CONFIGURACIÓN DE NAP E \_ SHV \_ \_**</dt> </dl> | *ConfigID* ya existe. La lista de los ID conocidos por NPS es diferente de la SHV.<br/> |



 

## <a name="remarks"></a>Comentarios

Una vez creada la nueva configuración por **NewConfig,** se deben usar los métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)y [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) para modificar la configuración según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





