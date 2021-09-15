---
title: tan
description: Devuelve la tangente del valor especificado.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- tan HLSL
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567809"
---
# <a name="tan"></a>tan

Devuelve la tangente del valor especificado.



| *ret* tan(*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado, en radianes.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Tangente del parámetro *x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

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

 

