---
title: Interfaz ID3DX11EffectTechnique (D3dx11effect.h)
description: Una interfaz ID3DX11EffectTechnique es una colección de pases. La duración de un objeto ID3DX11EffectTechnique es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interfaz ID3DX11EffectTechnique Direct3D 11
- Interfaz ID3DX11EffectTechnique Direct3D 11, descrita
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
ms.openlocfilehash: 4d8970ad1e75f37e8270a013d3830216ae128e41c03d4ad5245ac6ffc7615691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532357"
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
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obtener una anotación por índice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obtiene una anotación por nombre.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obtenga una descripción de la técnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obtener un paso por índice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obtenga un pase por nombre.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Pruebe una técnica para ver si contiene una sintaxis válida.<br/>       |



 

## <a name="remarks"></a>Comentarios

Un efecto contiene una o varias técnicas; cada técnica contiene uno o varios pases; cada paso contiene asignaciones de estado.

Para obtener una interfaz de técnica de efecto, llame a un método como [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Efectos 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





