---
title: Función ProcessIsolineTessFactors
description: Genera los factores de teselación redondeados para una isolínea.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Función ProcessIsolineTessFactors HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168466"
---
# <a name="processisolinetessfactors-function"></a>Función ProcessIsolineTessFactors

Genera los factores de teselación redondeados para una isolínea.

## <a name="syntax"></a>Sintaxis

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*RawDetailFactor* \[ En\]
</dt> <dd>

Tipo: **float**

Factor de detalle deseado.

</dd> <dt>

*RawDensityFactor* \[ En\]
</dt> <dd>

Tipo: **float**

Factor de densidad deseado.

</dd> <dt>

*RoundedDetailFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Factor de detalle redondeado que se fija a un intervalo que puede usar el teselador.

</dd> <dt>

*RoundedDensityFactor* \[ out\]
</dt> <dd>

Tipo: **float**

Factor de densidad redondeado con fijación a un intervalo que puede usar el teselador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




