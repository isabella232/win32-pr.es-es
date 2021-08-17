---
title: Método INapComponentConfig3 GetConfigFromID (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Método NAP GetConfigFromID
- Método GetConfigFromID NAP , interfaz INapComponentConfig3
- Interfaz INapComponentConfig3 NAP, método GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638704b5706b68b67f854a6a52b6c845be3fb757b596e9f5425f315c7d679fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368403"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3::GetConfigFromID (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **GetConfigFromID** para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configID* \[ En\]
</dt> <dd>

Valor que representa la configuración. Si *ConfigID* es **0**, el SHV debe devolver los datos de configuración predeterminados en *outdata*.

</dd> <dt>

*count* \[ out\]
</dt> <dd>

Tamaño, en bytes, de los datos de configuración devueltos en *outdata*.

</dd> <dt>

*outdata* \[ out\]
</dt> <dd>

En la devolución, una matriz BYTE que contiene los datos de configuración representados *por ConfigID*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes códigos de error según el resultado de esta operación.



| Código devuelto                                                                                                    | Descripción                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                          | La operación se realizó correctamente.<br/> |
| <dl> <dt>**NO \_ SE ENCONTRÓ LA CONFIGURACIÓN DE NAP E \_ SHV \_ \_ \_**</dt> </dl> | *No se encuentra ConfigID.*<br/>  |



 

## <a name="remarks"></a>Comentarios

El [**método NewConfig**](inapcomponentconfig3-newconfig.md) debe usarse para asignar datos de configuración para *ConfigID* antes de que se pueda llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





