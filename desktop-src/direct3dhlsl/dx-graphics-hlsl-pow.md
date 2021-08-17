---
title: pow
description: Devuelve el valor especificado elevado a la potencia especificada.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9d26e150d611df12f2e042d2e20c06ab82172bbc3d2f241ee1ce3a4725f1193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120079"
---
# <a name="pow"></a>pow

Devuelve el valor especificado elevado a la potencia especificada.



| *ret* pow(*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] La potencia especificada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parámetro *x* elevado a la potencia del *parámetro y.*

## <a name="remarks"></a>Comentarios

La función intrínseca HLSL **pow** calcula *x*<sup>y</sup>.



| X      | Y      | Resultado                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | cualquiera    | NAN                                                                         |
| >0 | == 0   | 1                                                                           |
| == 0   | >0 | 0                                                                           |
| == 0   | < 0 | inf                                                                         |
| >0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| == 0   | == 0   | Depende del procesador de gráficos concreto<br/> 0, o 1, o NAN<br/> |



 

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

