---
title: Interfaz ID3DX11EffectDepthStencilVariable (D3dx11effect.h)
description: Una interfaz depth-stencil-variable accede al estado depth-stencil.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Id3DX11EffectDepthStencilVariable interface Direct3D 11
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
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060822"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interfaz ID3DX11EffectDepthStencilVariable

Una interfaz depth-stencil-variable accede al estado depth-stencil.

## <a name="members"></a>Members

La **interfaz ID3DX11EffectDepthStencilVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectDepthStencilVariable** tiene estos métodos.



| Método                                                                                         | Descripción                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Obtiene un puntero a una variable que contiene el estado de galería de símbolos de profundidad.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Obtiene un puntero a una interfaz de galería de símbolos de profundidad.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Establece el estado de la galería de símbolos de profundidad.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Revierte un estado de galería de símbolos de profundidad establecido previamente.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Se [**crea una interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en memoria en el almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Puede usar cualquiera de estos métodos para devolver el estado.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





