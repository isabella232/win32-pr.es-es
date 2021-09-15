---
title: noise
description: Genera un valor aleatorio mediante el algoritmo perlin-noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HLSL de ruido
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258500"
---
# <a name="noise"></a>noise

Genera un valor aleatorio mediante el algoritmo perlin-noise.




| *ret* noise(*x*) |
|------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] Un vector de punto flotante a partir del cual se va a generar el ruido de Perlin.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de ruido de Perlin dentro de un intervalo entre -1 y 1.

## <a name="remarks"></a>Observaciones

Los valores de ruido de perlin cambian sin problemas de un punto a otro en un espacio, creando valores naturales generados aleatoriamente. Puede usar el ruido de Perlin para generar texturas de procedimientos para efectos como humo y incendio.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera  |
| *Ret* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | no                  |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo tx \_ 1 \_ 0) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

