---
title: Interfaz ID3DX11EffectTechnique (D3dx11effect.h)
description: Una interfaz ID3DX11EffectTechnique es una colección de pases. La duración de un objeto ID3DX11EffectTechnique es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interfaz ID3DX11EffectTechnique Direct3D 11
- Interfaz ID3DX11EffectTechnique Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476065"
---
# <a name="id3dx11effecttechnique-interface"></a>Interfaz ID3DX11EffectTechnique

Una **interfaz ID3DX11EffectTechnique** es una colección de pases.

La duración de **un objeto ID3DX11EffectTechnique** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectTechnique** tiene estos métodos.



| Método                                                                        | Descripción                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Calcule una máscara de bloque de estado para permitir o evitar cambios de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obtiene una anotación por índice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obtenga una anotación por nombre.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obtenga una descripción de la técnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obtener un paso por índice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obtenga un pase por nombre.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Pruebe una técnica para ver si contiene una sintaxis válida.<br/>       |



 

## <a name="remarks"></a>Observaciones

Un efecto contiene una o varias técnicas; cada técnica contiene uno o varios pases; cada paso contiene asignaciones de estado.

Para obtener una interfaz de técnica de efecto, llame a un método como [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





