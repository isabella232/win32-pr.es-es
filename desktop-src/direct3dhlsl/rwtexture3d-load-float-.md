---
title: 'RWTexture3D:: Load (int) (función)'
description: 'Lee los datos de textura. | RWTexture3D:: Load (int) (función)'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362219"
---
# <a name="rwtexture3dloadint-function"></a>RWTexture3D:: Load (int) (función)

Lee los datos de textura.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **int**

Ubicación de la textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture3D**](sm5-object-rwtexture3d.md) .

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cargar métodos](rwtexture3d-load.md)
</dt> </dl>

 

 




