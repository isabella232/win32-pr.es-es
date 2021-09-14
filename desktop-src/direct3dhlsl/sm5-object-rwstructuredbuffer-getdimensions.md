---
title: RwStructuredBuffer::GetDimensions (Función)
description: Obtiene las dimensiones de recursos. | RwStructuredBuffer::GetDimensions (Función)
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
keywords:
- Función GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174710"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>RwStructuredBuffer::GetDimensions (Función)

Obtiene las dimensiones de recursos.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*numStructs* \[ out\]
</dt> <dd>

Tipo: **uint**

Número de estructuras del recurso.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Tipo: **uint**

El paso, en bytes, de cada elemento de estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Nada

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




