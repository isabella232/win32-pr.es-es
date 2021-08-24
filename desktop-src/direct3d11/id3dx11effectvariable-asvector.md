---
title: Método ID3DX11EffectVariable AsVector (D3dx11effect.h)
description: Obtiene una variable de vector.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Método AsVector Direct3D 11
- Método AsVector Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5ce5023c0fd77109d91705c3faaf788b5f0e6edd3bd3ba15b7aeb367b8d061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119695"
---
# <a name="id3dx11effectvariableasvector-method"></a>Método ID3DX11EffectVariable::AsVector

Obtiene una variable de vector.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***

Puntero a una variable vectorial. Vea [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).

## <a name="remarks"></a>Comentarios

AsVector devuelve una versión de la variable de efecto que se ha especializado en una variable de vector. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos vectoriales.

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

 

 





