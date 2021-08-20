---
title: Interfaz ID3DX11EffectRasterizerVariable (D3dx11effect.h)
description: Una interfaz rasterizador-variable accede al estado del rasterizador.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11
- Id3DX11EffectRasterizerVariable interface Direct3D 11 , descrito
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4653936edc3fd2181f875b3a848e401b8fa24d318a1e48df4fa06e462ae3cf19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534191"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>Interfaz ID3DX11EffectRasterizerVariable

Una interfaz rasterizador-variable accede al estado del rasterizador.

## <a name="members"></a>Miembros

La **interfaz ID3DX11EffectRasterizerVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectRasterizerVariable** tiene estos métodos.



| Método                                                                                   | Descripción                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Obtiene un puntero a una variable que contiene el estado de rasteriser.<br/> |
| [**GetRasterizerState**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Obtenga un puntero a una interfaz de rasterizador.<br/>                    |
| [**SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Establece el estado del rasterizador.<br/>                                  |
| [**UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Revierte un estado de rasterizador establecido previamente.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Se [**crea una interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en memoria en el almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Puede usar cualquiera de estos métodos para devolver el estado.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfaces de Efectos 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





