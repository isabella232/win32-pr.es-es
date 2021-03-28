---
title: Método asvector ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene una variable de vector.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Método asvector de Direct3D 11
- Método asvector de Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método asvector
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
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998713"
---
# <a name="id3dx11effectvariableasvector-method"></a>ID3DX11EffectVariable:: asvector (método)

Obtiene una variable de vector.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***

Puntero a una variable de vector. Vea [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).

## <a name="remarks"></a>Observaciones

Asvector devuelve una versión de la variable de efecto que se ha especializado en una variable de vector. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos vectoriales.

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

 

 





