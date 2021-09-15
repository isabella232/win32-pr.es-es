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
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568040"
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

## <a name="remarks"></a>Observaciones

AsDepthStencil devuelve una versión de la variable de efecto que se ha especializado en una variable de galería de símbolos de profundidad. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de galería de símbolos de profundidad.

Las aplicaciones pueden probar la validez del objeto devuelto llamando a [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





