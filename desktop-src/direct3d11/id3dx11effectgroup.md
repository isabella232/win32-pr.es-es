---
title: Interfaz ID3DX11EffectGroup (D3dx11effect.h)
description: La interfaz ID3DX11EffectGroup tiene acceso a un grupo de efectos. La duración de un objeto ID3DX11EffectGroup es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaz ID3DX11EffectGroup Direct3D 11
- Interfaz ID3DX11EffectGroup Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa42a884be0abd15f0d16403a95d859d89cd472fc630b51ffe586e703e1a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046233"
---
# <a name="id3dx11effectgroup-interface"></a>Interfaz ID3DX11EffectGroup

La **interfaz ID3DX11EffectGroup** tiene acceso a un grupo de efectos.

La duración de **un objeto ID3DX11EffectGroup** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectGroup** tiene estos métodos.



| Método                                                                  | Descripción                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Obtiene una anotación por índice.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Obtenga una anotación por nombre.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Obtiene una descripción del grupo.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Obtenga una técnica por índice.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Obtenga una técnica por nombre.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Pruebe un efecto para ver si contiene una sintaxis válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener una **interfaz ID3DX11EffectGroup,** llame a un método como [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).

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

 

 





