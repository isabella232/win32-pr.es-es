---
title: Interfaz ID3DX11EffectTechnique (D3dx11effect. h)
description: Una interfaz ID3DX11EffectTechnique es una colección de pasadas. La duración de un objeto ID3DX11EffectTechnique es igual a la duración de su objeto ID3DX11Effect primario.
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
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987193"
---
# <a name="id3dx11effecttechnique-interface"></a>Interfaz ID3DX11EffectTechnique

Una interfaz **ID3DX11EffectTechnique** es una colección de pasadas.

La duración de un objeto **ID3DX11EffectTechnique** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectTechnique** tiene estos métodos.



| Método                                                                        | Descripción                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Obtiene una anotación por índice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Obtiene una anotación por nombre.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Obtener una descripción de la técnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Obtiene un paso por índice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Obtiene un paso por nombre.<br/>                                        |
| [**IsValid**](id3dx11effecttechnique-isvalid.md)                             | Pruebe una técnica para ver si contiene una sintaxis válida.<br/>       |



 

## <a name="remarks"></a>Observaciones

Un efecto contiene una o más técnicas; cada técnica contiene uno o varios pasos; cada paso contiene asignaciones de estado.

Para obtener una interfaz de la técnica de efectos, llame a un método como [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





