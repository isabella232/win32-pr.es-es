---
title: Método ID3DX11EffectVariable AsBlend (D3dx11effect.h)
description: Obtiene una variable de combinación de efecto.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Método AsBlend Direct3D 11
- Método AsBlend Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , Método AsBlend
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f7e3d09a1299d00482e9a5cfbb75f563d4bba5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465753"
---
# <a name="id3dx11effectvariableasblend-method"></a>Método ID3DX11EffectVariable::AsBlend

Obtiene una variable de combinación de efecto.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***

Puntero a una variable de combinación de efecto. Vea [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).

## <a name="remarks"></a>Observaciones

AsBlend devuelve una versión de la variable de efecto que se ha especializado en una variable de combinación de efecto. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de combinación de efecto.

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

 

 





