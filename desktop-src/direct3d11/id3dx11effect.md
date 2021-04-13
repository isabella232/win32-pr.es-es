---
title: Interfaz ID3DX11Effect (D3dx11effect. h)
description: Una interfaz ID3DX11Effect administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interfaz ID3DX11Effect Direct3D 11
- Interfaz ID3DX11Effect Direct3D 11, descrita
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
ms.openlocfilehash: 395946ea4276bc57595abdeb18e7d1755ca0ff1d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998598"
---
# <a name="id3dx11effect-interface"></a>Interfaz ID3DX11Effect

Una interfaz **ID3DX11Effect** administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.

## <a name="members"></a>Miembros

La interfaz **ID3DX11Effect** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11Effect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11Effect** tiene estos métodos.



| Método                                                                     | Descripción                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Crea una copia de una interfaz de efecto.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Obtiene una interfaz de vinculación de clases.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Obtiene un búfer de constantes por índice.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Obtiene un búfer de constantes por nombre.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Obtiene una descripción de efecto.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Obtiene el dispositivo que creó el efecto.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Obtiene un grupo de efectos por índice.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Obtiene un grupo de efectos por nombre.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Obtiene una técnica por índice.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Obtener una técnica por nombre.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Obtiene una variable por índice.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Obtiene una variable por nombre.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Obtiene una variable por semántica.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Pruebe un efecto para ver si los metadatos de reflexión se han quitado de la memoria.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Pruebe un efecto para ver si contiene una sintaxis válida.<br/>                             |
| [**Optimización**](id3dx11effect-optimize.md)                                 | Minimizar la cantidad de memoria necesaria para un efecto.<br/>                          |



 

## <a name="remarks"></a>Observaciones

Un efecto se crea llamando a [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

El sistema de efectos agrupa la información necesaria para la representación en un efecto que contiene: objetos de estado para asignar cambios de estado en grupos, recursos para proporcionar datos de entrada y almacenamiento de datos de salida, y programas que controlan cómo se realiza la representación denominado sombreadores.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

> [!Note]
>
> Si llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un objeto **ID3DX11Effect** para recuperar la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** devuelve E \_ nointerface. Para solucionar este problema, use el código siguiente:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="requirements"></a>Requisitos
>
> 
>
| Requisito | Valor |
> |--------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    | | Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |
>
> 
>
> ## <a name="see-also"></a>Vea también
>
> <dl> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>
>
>  
>
>  
>
