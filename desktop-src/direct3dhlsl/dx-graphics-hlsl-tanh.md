---
title: tanh
description: Devuelve la tangente hiperbólica del valor especificado.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072747"
---
# <a name="tanh"></a>tanh

Devuelve la tangente hiperbólica del valor especificado.



| *ret* tanh(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] el valor especificado, en radianes.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Tangente hiperbólica del *parámetro x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

