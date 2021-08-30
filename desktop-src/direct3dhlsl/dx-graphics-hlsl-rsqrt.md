---
title: rsqrt
description: Devuelve el recíproco de la raíz cuadrada del valor especificado.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- rsqrt HLSL
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bafea73a2063b09b81523f2706dc0f3aed57dabc61a49c64acf321002b1f4db7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950315"
---
# <a name="rsqrt"></a>rsqrt

Devuelve el recíproco de la raíz cuadrada del valor especificado.



| *ret* rsqrt(*x*) |
|------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Recíproco de la raíz cuadrada del *parámetro x.*

## <a name="remarks"></a>Comentarios

Esta función usa la fórmula siguiente: 1 / **sqrt**(*x*).

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

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

 

