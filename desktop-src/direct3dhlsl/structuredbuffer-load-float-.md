---
title: 'StructuredBuffer:: Load (int) (función)'
description: 'Lee los datos del búfer. | StructuredBuffer:: Load (int) (función)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986610"
---
# <a name="structuredbufferloadint-function"></a>StructuredBuffer:: Load (int) (función)

Lee los datos del búfer.

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

Ubicación del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cargar métodos](structuredbuffer-load.md)
</dt> </dl>

 

 




