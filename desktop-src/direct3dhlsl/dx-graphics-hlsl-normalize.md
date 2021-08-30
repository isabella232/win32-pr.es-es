---
title: Normalizar
description: Normaliza el vector de punto flotante especificado según x/ length(x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- normalizar HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01b14fb95e77542ab48e535add548514af22829644934abffdc845c27d3d96b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024305"
---
# <a name="normalize"></a>Normalizar

Normaliza el vector de punto flotante especificado según x/ length(x).



| *ret* normalize(*x*) |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El vector de punto flotante especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parámetro *x* normalizado. Si la longitud del *parámetro x* es 0, el resultado es indefinido.

## <a name="remarks"></a>Comentarios

La **función intrínseca normalize** HLSL usa la fórmula siguiente: *x*  /  [**length**](dx-graphics-hlsl-length.md)(*x*).

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                   | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

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

 

