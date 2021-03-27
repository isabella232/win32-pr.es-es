---
title: Interfaz ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Una interfaz de nivel de estarcido de profundidad tiene acceso a un estado de estarcido de profundidad.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, descrita
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003931"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interfaz ID3DX11EffectDepthStencilVariable

Una interfaz de nivel de estarcido de profundidad tiene acceso a un estado de estarcido de profundidad.

## <a name="members"></a>Miembros

La interfaz **ID3DX11EffectDepthStencilVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectDepthStencilVariable** tiene estos métodos.



| Método                                                                                         | Descripción                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Obtiene un puntero a una interfaz de estarcido de profundidad.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Establece el estado de la galería de símbolos de profundidad.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Revierte un estado de estarcido de profundidad establecido previamente.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Una interfaz [**ID3DX11EffectVariable**](id3dx11effectvariable.md) se crea cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo. Puede utilizar cualquiera de estos métodos para devolver el estado.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





