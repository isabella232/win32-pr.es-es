---
title: Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
description: Obtiene un búfer de constantes. | Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Método AsConstantBuffer Direct3D 11
- Método AsConstantBuffer Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método AsConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998431"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a>ID3DX11EffectVariable:: AsConstantBuffer (método)

Obtiene un búfer de constantes.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Un puntero a un búfer de constantes. Vea [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Observaciones

AsConstantBuffer devuelve una versión de la variable de efecto que se ha especializado en un búfer de constantes. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de búfer de constantes.

Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





