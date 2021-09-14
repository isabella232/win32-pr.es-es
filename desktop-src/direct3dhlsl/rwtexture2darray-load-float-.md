---
title: Función RWTexture2DArray::Load(int)
description: Lee los datos de textura. | Función RWTexture2DArray::Load(int)
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
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
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160417"
---
# <a name="rwtexture2darrayloadint-function"></a>Función RWTexture2DArray::Load(int)

Lee los datos de textura.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int**

Ubicación de la textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración para el [**objeto RWTexture2DArray.**](sm5-object-rwtexture2darray.md)

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de carga](rwtexture2darray-load.md)
</dt> </dl>

 

 




