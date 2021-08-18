---
title: Interfaz ID3DX11EffectDepthStencilVariable (D3dx11effect.h)
description: Una interfaz depth-stencil-variable accede al estado de la galería de símbolos de profundidad.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11
- Id3DX11EffectDepthStencilVariable interface Direct3D 11 , descrito
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d743bfebfa9722261d220800a633bdc8b268a520b883c9fea11f9f7948f7bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989775"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interfaz ID3DX11EffectDepthStencilVariable

Una interfaz depth-stencil-variable accede al estado de la galería de símbolos de profundidad.

## <a name="members"></a>Miembros

La **interfaz ID3DX11EffectDepthStencilVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectDepthStencilVariable** tiene estos métodos.



| Método                                                                                         | Descripción                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Obtiene un puntero a una interfaz de galería de símbolos de profundidad.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Establece el estado de la galería de símbolos de profundidad.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Revierte un estado de galería de símbolos de profundidad establecido previamente.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Se [**crea una interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en la memoria del almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Puede usar cualquiera de estos métodos para devolver el estado.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





