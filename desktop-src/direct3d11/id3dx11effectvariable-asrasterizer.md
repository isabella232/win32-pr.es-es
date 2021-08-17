---
title: Método AsRasterizer ID3DX11EffectVariable (D3dx11effect.h)
description: Obtiene una variable de rasterizador.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Método AsRasterizer Direct3D 11
- Método AsRasterizer Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsRasterizer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfaf83debc6c7e73a89f78b0c8c3899cce2fb83fb6a5884fa5a5ed9ed5b35912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858105"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>Método ID3DX11EffectVariable::AsRasterizer

Obtiene una variable de rasterizador.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Puntero a una variable rasterizadora. Vea [**ID3DX11EffectRasterizerVariable.**](id3dx11effectrasterizervariable.md)

## <a name="remarks"></a>Comentarios

AsRasterizer devuelve una versión de la variable de efecto que se ha especializado en una variable rasterizadora. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de rasterizador.

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

 

 





