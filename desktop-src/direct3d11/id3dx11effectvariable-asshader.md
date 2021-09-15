---
title: Método ASShader ID3DX11EffectVariable (D3dx11effect.h)
description: Obtiene una variable de sombreador.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Método AsShader Direct3D 11
- Método AsShader Direct3D 11 , interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsShader
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568009"
---
# <a name="id3dx11effectvariableasshader-method"></a>Método ID3DX11EffectVariable::AsShader

Obtiene una variable de sombreador.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

Puntero a una variable de sombreador. Vea [**ID3DX11EffectShaderVariable.**](id3dx11effectshadervariable.md)

## <a name="remarks"></a>Observaciones

AsShader devuelve una versión de la variable de efecto que se ha especializado en una variable de sombreador. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de sombreador.

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

 

 





