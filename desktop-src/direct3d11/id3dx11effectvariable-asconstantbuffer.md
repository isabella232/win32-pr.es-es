---
title: Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect.h)
description: Obtiene un búfer constante. | Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect.h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Método AsConstantBuffer Direct3D 11
- Método AsConstantBuffer Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsConstantBuffer
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568041"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a>Método ID3DX11EffectVariable::AsConstantBuffer

Obtiene un búfer constante.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntero a un búfer constante. Vea [**ID3DX11EffectConstantBuffer.**](id3dx11effectconstantbuffer.md)

## <a name="remarks"></a>Observaciones

AsConstantBuffer devuelve una versión de la variable de efecto que se ha especializado en un búfer constante. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de búfer constante.

Las aplicaciones pueden probar la validez del objeto devuelto llamando a [**IsValid.**](id3dx11effectvariable-isvalid.md)

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





