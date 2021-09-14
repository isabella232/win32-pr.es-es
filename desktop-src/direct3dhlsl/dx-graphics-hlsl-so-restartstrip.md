---
title: RestartStrip (objeto Stream-Output HLSL de DirectX)
description: Finaliza la franja primitiva actual e inicia una nueva. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará la primitiva incompleta al final.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969607"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (objeto Stream-Output HLSL de DirectX)

Finaliza la franja primitiva actual e inicia una nueva. Si la franja actual no tiene suficientes vértices emitidos para rellenar la topología primitiva, se descartará la primitiva incompleta al final.

RestartStrip();



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                     | Descripción |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno**<br/> |             |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="remarks"></a>Observaciones

Un corte de franja hace que la franja actual finalice y se inicie una nueva. Un corte de franja se puede realizar llamando explícitamente a este método o simplemente representando hasta el valor de índice máximo ( 1, que es 0xffffffff para índices de 32 bits o 0xffff para índices de 16 bits). Cada instancia de un dibujo de instancia indizada genera automáticamente un corte de franja. Esto es así incluso si la topología no es una franja de triángulos.

> [!Note]  
> La compatibilidad con el reinicio y el 1 "valor mágico" para un corte solo está disponible en los dispositivos [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) nivel de característica 10.0 o superior.

 

Siempre se supone que la salida es una franja de triángulos. Para convertir la salida en una lista de triángulos, debe llamar a RestartStrip entre cada triángulo. No se admiten los ventiladores de triángulo.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

