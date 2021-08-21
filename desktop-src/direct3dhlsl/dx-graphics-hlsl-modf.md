---
title: modf (Corecrt \_ math.h)
description: Divide el valor x en partes fraccionales y enteras, cada una de las cuales tiene el mismo signo que x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c09af44cb95f35854d4366c05d238423fcecaff7c9a10c3c55fadf6b51dd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513816"
---
# <a name="modf"></a>modf

Divide el valor x en partes fraccionales y enteras, cada una de las cuales tiene el mismo signo que x.



| ret modf(x, out ip) |
|---------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                      | Descripción                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>    | \[en \] El valor de entrada x.<br/>           |
| <span id="ip"></span><span id="IP"></span>*Ip*<br/> | \[out \] La parte entera de *x*.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Parte con firma fraccional de x.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in     | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                          |
| ip   | out    | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada x |
| Ret  | out    | igual que la entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada x |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

