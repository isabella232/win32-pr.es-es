---
title: Método ID3DX11EffectVariable AsSampler (D3dx11effect.h)
description: Obtenga una variable sampler.
ms.assetid: dff699f7-758a-442b-93eb-23a09468251f
keywords:
- Método AsSampler Direct3D 11
- Método AsSampler Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1213320950377f6981348a158c3d8c8ef4d4fd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465561"
---
# <a name="id3dx11effectvariableassampler-method"></a>Método ID3DX11EffectVariable::AsSampler

Obtenga una variable sampler.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectSamplerVariable* AsSampler();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)\***

Puntero a una variable sampler. Vea [**ID3DX11EffectSamplerVariable.**](id3dx11effectsamplervariable.md)

## <a name="remarks"></a>Observaciones

AsSampler devuelve una versión de la variable de efecto que se ha especializado en una variable sampler. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de sampler.

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

 

 





