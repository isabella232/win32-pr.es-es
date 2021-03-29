---
title: GetRenderTargetSampleCount
description: Obtiene el número de muestras para un destino de representación.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL de GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487162"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Obtiene el número de muestras para un destino de representación.



| *Uint* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                 | Descripción |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguna<br/> |             |



 

## <a name="return-value"></a>Valor devuelto

Número de muestras.

## <a name="remarks"></a>Observaciones

Use esta función y [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) para averiguar el número y la posición de las ubicaciones de muestreo para un destino de representación.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





