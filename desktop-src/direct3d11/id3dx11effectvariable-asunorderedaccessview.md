---
title: Método ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect.h)
description: Obtiene una variable unordered-access-view.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Método AsUnorderedAccessView Direct3D 11
- Método AsUnorderedAccessView Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11 , método AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cf3a1f146af7ca6faf3ff3e704285ac19f01a117809429842b45df9b7dcfd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531213"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a>Método ID3DX11EffectVariable::AsUnorderedAccessView

Obtiene una variable unordered-access-view.

## <a name="syntax"></a>Sintaxis


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***

Puntero a una variable unordered-access-view. Vea [**ID3DX11EffectUnorderedAccessViewVariable.**](id3dx11effectunorderedaccessviewvariable.md)

## <a name="remarks"></a>Comentarios

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

 

 





