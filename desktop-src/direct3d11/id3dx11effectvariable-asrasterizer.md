---
title: Método ASRasterizer ID3DX11EffectVariable (D3dx11effect.h)
description: Obtiene una variable rasterizadora.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Método AsRasterizer Direct3D 11
- Método AsRasterizer Direct3D 11 , interfaz ID3DX11EffectVariable
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
ms.openlocfilehash: 2cbe4edc1b1195a9d449b37897f0875b1f35aae3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568016"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>Método ID3DX11EffectVariable::AsRasterizer

Obtiene una variable rasterizadora.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Puntero a una variable rasterizadora. Vea [**ID3DX11EffectRasterizerVariable.**](id3dx11effectrasterizervariable.md)

## <a name="remarks"></a>Observaciones

AsRasterizer devuelve una versión de la variable de efecto que se ha especializado en una variable rasterizadora. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de rasterizador.

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

 

 





