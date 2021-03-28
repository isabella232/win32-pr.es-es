---
title: Método ID3DX11EffectVariable AsShaderResource (D3dx11effect. h)
description: Obtiene una variable de recurso de sombreador.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Método AsShaderResource Direct3D 11
- Método AsShaderResource Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método AsShaderResource
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3af6236d25e8a2c652f5a551bf7199f3a78d8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998773"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a>ID3DX11EffectVariable:: AsShaderResource (método)

Obtiene una variable de recurso de sombreador.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***

Puntero a una variable de recurso de sombreador. Vea [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).

## <a name="remarks"></a>Observaciones

AsShaderResource devuelve una versión de la variable de efecto que se ha especializado en una variable de recurso de sombreador. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de recursos de sombreador.

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

 

 





