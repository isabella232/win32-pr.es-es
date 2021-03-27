---
title: ProcessIsolineTessFactors función)
description: Genera los factores de teselación redondeada para un Isoline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors de función HLSL
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784355"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors función)

Genera los factores de teselación redondeada para un Isoline.

## <a name="syntax"></a>Sintaxis

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*RawDetailFactor* \[ de\]
</dt> <dd>

Tipo: **float**

Factor de detalle deseado.

</dd> <dt>

*RawDensityFactor* \[ de\]
</dt> <dd>

Tipo: **float**

Factor de densidad deseado.

</dd> <dt>

*RoundedDetailFactor* \[ enuncia\]
</dt> <dd>

Tipo: **float**

Factor de detalle redondeado con un intervalo que puede usar el del teselador.

</dd> <dt>

*RoundedDensityFactor* \[ enuncia\]
</dt> <dd>

Tipo: **float**

El factor de densidad redondeada fijado a un rangethat puede ser utilizado por el del teselador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




