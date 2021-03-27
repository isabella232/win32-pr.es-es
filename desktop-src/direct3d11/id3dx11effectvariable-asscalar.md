---
title: Método asescalar ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene una variable escalar.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Asescalar método Direct3D 11
- Método asescalar Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, asescalate (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821543"
---
# <a name="id3dx11effectvariableasscalar-method"></a>ID3DX11EffectVariable:: asescalate (método)

Obtiene una variable escalar.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***

Puntero a una variable escalar. Vea [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).

## <a name="remarks"></a>Observaciones

Asescalar devuelve una versión de la variable de efecto que se ha especializado en una variable escalar. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos escalares.

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

 

 





