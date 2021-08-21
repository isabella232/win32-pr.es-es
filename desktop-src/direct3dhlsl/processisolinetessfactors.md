---
title: Función ProcessIsolineTessFactors
description: Genera los factores de teselación redondeados para una isolínea.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Función HLSL de ProcessIsolineTessFactors
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986295"
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

Factor de densidad redondeado que se fija a un intervalo que puede usar el teselador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




