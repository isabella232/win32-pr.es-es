---
title: Interfaz ID3DX11EffectBlendVariable (D3dx11effect.h)
description: La interfaz blend-variable accede al estado de blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interfaz ID3DX11EffectBlendVariable direct3D 11
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bd65c15c40c2e7ce44092baebdef66f17f2de8c1052589a984ff15c9f4b77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046463"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interfaz ID3DX11EffectBlendVariable

La interfaz blend-variable accede al estado de blend.

## <a name="members"></a>Miembros

La **interfaz ID3DX11EffectBlendVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectBlendVariable** tiene estos métodos.



| Método                                                                    | Descripción                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Obtiene un puntero a una variable de estado de mezcla.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Obtiene un puntero a una interfaz de estado de mezcla.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Establece el estado de mezcla de un efecto.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Revierte un estado de mezcla establecido previamente.<br/>     |



 

## <a name="remarks"></a>Comentarios

Se [**crea una interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en memoria en el almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Puede usar cualquiera de estos métodos para devolver el estado.

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

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





