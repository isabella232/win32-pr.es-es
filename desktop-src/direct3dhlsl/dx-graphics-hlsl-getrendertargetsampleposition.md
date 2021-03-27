---
title: GetRenderTargetSamplePosition
description: Obtiene la posición de muestreo (x, y) de un índice de ejemplo determinado.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL de GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783311"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Obtiene la posición de muestreo (x, y) de un índice de ejemplo determinado.



|                                                                                  |
|----------------------------------------------------------------------------------|
| Float<2> GetRenderTargetSamplePosition (en int<1> index<br/>); |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                       | Descripción                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Ajustar*<br/> | \[en \] un índice de ejemplo basado en cero.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Posición (x, y) del ejemplo determinado.

## <a name="remarks"></a>Observaciones

Use esta función y [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) para averiguar el número y la posición de las ubicaciones de muestreo para un destino de representación.

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

 

 





