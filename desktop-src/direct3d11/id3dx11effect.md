---
title: Interfaz ID3DX11Effect (D3dx11effect.h)
description: Una interfaz ID3DX11Effect administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11Effect interface Direct3D 11
- ID3DX11Effect interface Direct3D 11 , descrito
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479151"
---
# <a name="id3dx11effect-interface"></a>Interfaz ID3DX11Effect

Una **interfaz ID3DX11Effect** administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.

## <a name="members"></a>Miembros

La **interfaz ID3DX11Effect** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11Effect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11Effect** tiene estos métodos.



| Método                                                                     | Descripción                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Crea una copia de una interfaz de efecto.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Obtiene una interfaz de vinculación de clases.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Obtener un búfer constante por índice.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Obtenga un búfer constante por nombre.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Obtiene una descripción del efecto.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Obtenga el dispositivo que creó el efecto.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Obtiene un grupo de efectos por índice.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Obtiene un grupo de efectos por nombre.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Obtenga una técnica por índice.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Obtenga una técnica por nombre.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Obtener una variable por índice.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Obtenga una variable por nombre.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Obtener una variable por semántica.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Pruebe un efecto para ver si contiene una sintaxis válida.<br/>                             |
| [**Optimización**](id3dx11effect-optimize.md)                                 | Minimice la cantidad de memoria necesaria para un efecto.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Se crea un efecto llamando a [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

El sistema de efectos agrupa la información necesaria para la representación en un efecto que contiene: objetos de estado para asignar cambios de estado en grupos, recursos para proporcionar datos de entrada y almacenar datos de salida, y programas que controlan cómo se realiza la representación denominados sombreadores.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

> [!Note]
>
> Si llama a [**QueryInterface en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) un **objeto ID3DX11Effect** para recuperar la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **QueryInterface** devuelve E \_ NOINTERFACE. Para evitar este problema, use el código siguiente:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |

## <a name="see-also"></a>Consulte también

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
