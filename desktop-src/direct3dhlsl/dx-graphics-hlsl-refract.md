---
title: Refractan
description: Devuelve un vector de retracción mediante un rayo de entrada, un normal de superficie y un índice de retracción.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- reescríbalo HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3895f39d7559fbc8707d3306d8183bfcef60890fa0393a788d17822137b8de2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090982"
---
# <a name="refract"></a>Refractan

Devuelve un vector de retracción mediante un rayo de entrada, un normal de superficie y un índice de retracción.



| *ret* refracción(*i*, *n*, ?) |
|----------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*i*<br/> | \[en \] Un vector de dirección de rayo de punto flotante.<br/>    |
| <span id="n"></span><span id="N"></span>*N*<br/> | \[en \] Un vector normal de superficie de punto flotante.<br/>   |
| *?*<br/>                                         | \[en \] un valor escalar de punto flotante, índice de retracción.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Vector de retracción de punto flotante. Si el ángulo entre el rayo de entrada i y la superficie normal n es demasiado grande para un índice de retracción determinado?, el valor devuelto es (0,0,0).

## <a name="type-description"></a>Descripción del tipo



| Nombre              | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *n*               | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *i* |
| ?                 | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| vector de reestracción | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *i* |



 

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

 

