---
title: discard (sm4 - asm)
description: Marca condicionalmente los resultados del sombreador de píxeles que se descartarán cuando se alcance el final del programa.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6b5744ee8cf8d2953247711d95fe5d5ec6f96c36c700e1a38ce4e0cb1e1ff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986605"
---
# <a name="discard-sm4---asm"></a>discard (sm4 - asm)

Marca condicionalmente los resultados del sombreador de píxeles que se descartarán cuando se alcance el final del programa.



| discard{ \_ z\|\_Componente nz} src0.select \_ |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor que determina si se debe descartar el píxel actual que se está procesando.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción marca el píxel actual como finalizado, mientras continúa la ejecución, de modo que otros píxeles que se ejecutan en paralelo puedan obtener derivados si es necesario. Aunque la ejecución continúa, se descartan todas  las salidas del sombreador de píxeles antes o después de la instrucción de descarte.

Para **descartar \_ z**, si todos los bits del *componente src0.select \_* son cero, se descarta el píxel.

Para **descartar \_ nz**, si los bits del componente *\_ src0.select* son distintos de cero, se descarta el píxel.

Además, la instrucción **de descarte** puede estar presente dentro de cualquier construcción de control de flujo.

Puede **haber varias** instrucciones de descarte en un sombreador y, si se ejecuta alguna, el píxel finaliza.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





