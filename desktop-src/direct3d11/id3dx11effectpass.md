---
title: Interfaz ID3DX11EffectPass (D3dx11effect.h)
description: Una interfaz ID3DX11EffectPass encapsula las asignaciones de estado dentro de una técnica. La duración de un objeto ID3DX11EffectPass es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interfaz ID3DX11EffectPass direct3D 11
- Interfaz ID3DX11EffectPass direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b24fe0154e447cd993e8e7e939a9a023ed37183a56980dab8f5d803a0ea41e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045983"
---
# <a name="id3dx11effectpass-interface"></a>Interfaz ID3DX11EffectPass

Una **interfaz ID3DX11EffectPass** encapsula las asignaciones de estado dentro de una técnica.

La duración de **un objeto ID3DX11EffectPass** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectPass** tiene estos métodos.



| Método                                                                   | Descripción                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Aplicar**](id3dx11effectpass-apply.md)                                 | Establezca el estado contenido en un paso al dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Genere una máscara para permitir o evitar cambios de estado.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Obtiene una anotación por índice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Obtiene una anotación por nombre.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Obtiene una descripción del sombreador de proceso.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Obtenga una descripción de paso.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Obtiene una descripción del sombreador de dominio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Obtiene una descripción del sombreador de geometría.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Obtiene la descripción del sombreador de casco.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Obtiene una descripción del sombreador de píxeles.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Obtiene una descripción del sombreador de vértices.<br/>                       |
| [**IsValid**](id3dx11effectpass-isvalid.md)                             | Pruebe un paso para ver si contiene una sintaxis válida.<br/>        |



 

## <a name="remarks"></a>Observaciones

Un paso es un bloque de código que establece objetos de estado de representación y sombreadores. Un paso se declara dentro de una técnica.

Para obtener una interfaz de paso de efecto, llame a un método como [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





