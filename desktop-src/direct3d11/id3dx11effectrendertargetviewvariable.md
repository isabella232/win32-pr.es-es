---
title: Interfaz ID3DX11EffectRenderTargetViewVariable (D3dx11effect.h)
description: Una interfaz render-target-view accede a un destino de representación.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358896"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>Interfaz ID3DX11EffectRenderTargetViewVariable

Una interfaz render-target-view accede a un destino de representación.

## <a name="members"></a>Members

La **interfaz ID3DX11EffectRenderTargetViewVariable** hereda de [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md). **ID3DX11EffectRenderTargetViewVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectRenderTargetViewVariable** tiene estos métodos.



| Método                                                                                     | Descripción                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Obtener un destino de representación.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Obtiene una matriz de destinos de representación.<br/> |
| [**SetRenderTarget**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Establezca un destino de representación.<br/>            |
| [**SetRenderTargetArray**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Establezca una matriz de destinos de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





