---
title: Método ID3DX11EffectVariable AsDepthStencil (D3dx11effect.h)
description: Obtiene una variable de galería de símbolos de profundidad.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Método AsDepthStencil Direct3D 11
- Método AsDepthStencil Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771f22b6b757b9144fca7e2637a3a702232b3d2a4a837938454b2acd5237cfae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729135"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a>Método ID3DX11EffectVariable::AsDepthStencil

Obtiene una variable de galería de símbolos de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***

Puntero a una variable de galería de símbolos de profundidad. Vea [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).

## <a name="remarks"></a>Comentarios

AsDepthStencil devuelve una versión de la variable de efecto que se ha especializado en una variable de galería de símbolos de profundidad. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de galería de símbolos de profundidad.

Las aplicaciones pueden probar la validez del objeto devuelto llamando a [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





