---
title: D3DCOLORtoUBYTE4
description: Convierte un vector 4D de punto flotante establecido por D3DCOLOR en un UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888324"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Convierte un vector 4D de punto flotante establecido por D3DCOLOR en un UBYTE4.



| *ret* D3DCOLORtoUBYTE4(*x*) |
|-----------------------------|



 

Esta función desliza y escala los componentes del *parámetro x.* Use esta función para compensar la falta de compatibilidad con UBYTE4 en algún hardware.

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] vector4 de punto flotante que se convertirá.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Representación UBYTE4 del *parámetro x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *Ret* | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Entero**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

