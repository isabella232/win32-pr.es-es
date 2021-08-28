---
title: Método ID3DX11EffectVariable AsDepthStencilView (D3dx11effect.h)
description: Obtiene una variable depth-stencil-view.
ms.assetid: 491ca6e1-a74c-4996-a25c-ea40910f0f36
keywords:
- Método AsDepthStencilView Direct3D 11
- Método AsDepthStencilView Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsDepthStencilView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencilView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dc0ce53478da8d7057c142c87daea5fb83503b4ac7cd1a0dee5edda89246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531516"
---
# <a name="id3dx11effectvariableasdepthstencilview-method"></a>Método ID3DX11EffectVariable::AsDepthStencilView

Obtiene una variable depth-stencil-view.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectDepthStencilViewVariable* AsDepthStencilView();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***

Puntero a una variable de vista de galería de símbolos de profundidad. Vea [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).

## <a name="remarks"></a>Comentarios

Este método devuelve una versión de la variable de efecto que se ha especializado en una variable de vista de galería de símbolos de profundidad. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de vista de galería de símbolos de profundidad.

Las aplicaciones pueden probar la validez del objeto devuelto llamando a [**IsValid.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





