---
title: RestartStrip (objeto de Stream-Output de DirectX HLSL)
description: Finaliza la franja primitiva actual e inicia una nueva banda. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará el primitivo incompleto en el extremo.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997080"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (objeto de Stream-Output de DirectX HLSL)

Finaliza la franja primitiva actual e inicia una nueva banda. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará el primitivo incompleto en el extremo.



|                 |
|-----------------|
| RestartStrip(); |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                     | Descripción |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguna**<br/> |             |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="remarks"></a>Observaciones

Un corte de franja hace que finalice la franja actual y se inicie una nueva. Un corte de franja se puede hacer llamando explícitamente a este método o simplemente representando hasta el valor de índice máximo (1, que es 0xFFFFFFFF para índices de 32 bits o 0xFFFF para índices de 16 bits). Cada instancia de un dibujo de instancia indizada genera automáticamente un corte de franja. Esto es así incluso si la topología no es una franja de triángulo.

> [!Note]  
> La compatibilidad con el reinicio y el 1 valor mágico para un corte solo está disponible en dispositivos de [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 o superior.

 

Siempre se supone que la salida es una franja de triángulo. Para que el resultado sea una lista de triángulos, debe llamar a RestartStrip entre cada triángulo. No se admiten los ventiladores de triángulo.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Stream: salida de objeto](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

