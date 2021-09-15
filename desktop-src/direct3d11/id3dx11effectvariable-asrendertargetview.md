---
title: Método ID3DX11EffectVariable AsRenderTargetView (D3dx11effect.h)
description: Obtiene una variable render-target-view.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Método AsRenderTargetView Direct3D 11
- Método AsRenderTargetView Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca6270503ff786b3f4a319e3f068ba76acada7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568017"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>Método ID3DX11EffectVariable::AsRenderTargetView

Obtiene una variable render-target-view.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Puntero a una variable render-target-view. Vea [**ID3DX11EffectRenderTargetViewVariable.**](id3dx11effectrendertargetviewvariable.md)

## <a name="remarks"></a>Observaciones

Este método devuelve una versión de la variable de efecto que se ha especializado en una variable render-target-view. De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de vista de destino de representación.

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

 

 





