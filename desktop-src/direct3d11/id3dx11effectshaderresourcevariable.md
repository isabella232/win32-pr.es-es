---
title: Interfaz ID3DX11EffectShaderResourceVariable (D3dx11effect.h)
description: Una interfaz de recurso de sombreador tiene acceso a un recurso de sombreador.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interfaz ID3DX11EffectShaderResourceVariable direct3D 11
- Interfaz ID3DX11EffectShaderResourceVariable direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476091"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>Interfaz ID3DX11EffectShaderResourceVariable

Una interfaz de recurso de sombreador tiene acceso a un recurso de sombreador.

## <a name="members"></a>Members

La **interfaz ID3DX11EffectShaderResourceVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectShaderResourceVariable** tiene estos métodos.



| Método                                                                           | Descripción                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Obtiene un recurso de sombreador.<br/>            |
| [**GetResourceArray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Obtiene una matriz de recursos de sombreador.<br/> |
| [**SetResource**](id3dx11effectshaderresourcevariable-setresource.md)           | Establezca un recurso de sombreador.<br/>            |
| [**SetResourceArray**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Establezca una matriz de recursos de sombreador.<br/> |



 

## <a name="remarks"></a>Observaciones

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

 

 





