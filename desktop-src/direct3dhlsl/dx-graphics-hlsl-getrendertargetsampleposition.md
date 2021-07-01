---
title: GetRenderTargetSamplePosition
description: Obtiene la posición de muestreo (x,y) de un índice de ejemplo determinado.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120580"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Obtiene la posición de muestreo (x,y) de un índice de ejemplo determinado.

float<2> GetRenderTargetSamplePosition( in int<1> Index<br/>);



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                       | Descripción                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Índice*<br/> | \[en \] un índice de ejemplo de base cero.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Posición (x,y) del ejemplo dado.

## <a name="remarks"></a>Observaciones

Use esta función y [**GetRenderTargetSampleCount para**](dx-graphics-hlsl-getrendertargetsamplecount.md) averiguar el número y la posición de las ubicaciones de muestreo de un destino de representación.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y modelos de sombreador posteriores | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





