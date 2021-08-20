---
title: clip
description: Descarta el píxel actual si el valor especificado es menor que cero.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- clip HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f12c9ea508aa960b0f3b1ec255867fc8e4f37fbee580ee5517ba40cf3ae0d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091073"
---
# <a name="clip"></a>clip

Descarta el píxel actual si el valor especificado es menor que cero.



| clip(*x*) |
|-----------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Comentarios

Use la **función intrínseca** HLSL de recorte para simular planos de recorte si cada componente del parámetro *x* representa la distancia desde un plano.

Además, use la **función clip** para probar el comportamiento alfa, como se muestra en el ejemplo siguiente:


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a>Descripción del tipo



| Nombre | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*  | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera  |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible               |
|-----------------------------------------------------------|-------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | sí (solo sombreador de píxeles) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

