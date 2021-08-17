---
title: GetRenderTargetSampleCount
description: Obtiene el número de ejemplos para un destino de representación.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120139"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Obtiene el número de ejemplos para un destino de representación.



| *UINT* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                 | Descripción |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguno<br/> |             |



 

## <a name="return-value"></a>Valor devuelto

Número de ejemplos.

## <a name="remarks"></a>Comentarios

Use esta función y [**GetRenderTargetSamplePosition para**](dx-graphics-hlsl-getrendertargetsampleposition.md) averiguar el número y la posición de las ubicaciones de muestreo de un destino de representación.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





