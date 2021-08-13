---
title: Efectos 11 Interfaces
description: Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) del origen Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537707"
---
# <a name="effects-11-interfaces"></a>Efectos 11 Interfaces

Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) del origen Effects 11.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Una [**interfaz ID3DX11Effect**](id3dx11effect.md) administra un conjunto de objetos de estado, recursos y sombreadores para implementar un efecto de representación.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | La interfaz blend-variable accede al estado de blend.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Tiene acceso a una instancia de clase.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Una interfaz de búfer constante tiene acceso a búferes constantes o búferes de textura.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Una interfaz depth-stencil-variable accede al estado de la galería de símbolos de profundidad.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Una interfaz depth-stencil-view-variable accede a una vista de galería de símbolos de profundidad.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | La [**interfaz ID3DX11EffectGroup**](id3dx11effectgroup.md) tiene acceso a un grupo de efectos.<br/> La duración de [**un objeto ID3DX11EffectGroup**](id3dx11effectgroup.md) es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Tiene acceso a una variable de interfaz.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Una interfaz de matriz y variable accede a una matriz.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Una [**interfaz ID3DX11EffectPass**](id3dx11effectpass.md) encapsula las asignaciones de estado dentro de una técnica.<br/> La duración de [**un objeto ID3DX11EffectPass**](id3dx11effectpass.md) es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Una interfaz rasterizador-variable accede al estado del rasterizador.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Una interfaz render-target-view tiene acceso a un destino de representación.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Una interfaz de sampler tiene acceso al estado del sampler.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Una interfaz effect-scalar-variable tiene acceso a valores escalares.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Una interfaz de recurso de sombreador tiene acceso a un recurso de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Una interfaz de variable de sombreador tiene acceso a una variable de sombreador.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Una interfaz de variable de cadena tiene acceso a una variable de cadena.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Una [**interfaz ID3DX11EffectTechnique**](id3dx11effecttechnique.md) es una colección de pases.<br/> La duración de [**un objeto ID3DX11EffectTechnique**](id3dx11effecttechnique.md) es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | La [**interfaz ID3DX11EffectType**](id3dx11effecttype.md) tiene acceso a las variables de efecto por tipo.<br/> La duración de [**un objeto ID3DX11EffectType**](id3dx11effecttype.md) es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Accede a una vista de acceso no ordenado.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | La [**interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) es la clase base para todas las variables de efecto.<br/> La duración de [**un objeto ID3DX11EffectVariable**](id3dx11effectvariable.md) es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Una interfaz vector-variable accede a un vector de cuatro componentes.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efectos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





