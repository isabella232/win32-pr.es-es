---
description: 'Esta sección contiene información sobre las siguientes interfaces del sistema de efectos:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfaces de efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303978"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfaces de efecto (Direct3D 10)

Esta sección contiene información sobre las siguientes interfaces del sistema de efectos:



| Interfaces                                                                                     | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interfaz ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Accede al estado de mezcla.                                            |
| [**Interfaz ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Tiene acceso a un búfer de textura o a un búfer constante.                  |
| [**Interfaz ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Accede al estado de galería de símbolos de profundidad.                                    |
| [**Interfaz ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Accede a una vista de galería de símbolos de profundidad.                                   |
| [**Interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Encapsula el estado de la canalización en una o varias técnicas de representación. |
| [**Interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Métodos implementados por el usuario para leer archivos de incluyen.              |
| [**Id3D10EffectMatrixVariable (interfaz)**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Accede a una matriz.                                               |
| [**Interfaz ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Encapsula el estado del efecto en un paso.                             |
| [**Interfaz ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica variables de efecto compartido.                              |
| [**Interfaz ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Accede al estado del rasterizador.                                       |
| [**Interfaz ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Tiene acceso a un destino de representación.                                        |
| [**Interfaz ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Accede al estado del sampler.                                          |
| [**Interfaz ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Tiene acceso a una variable escalar.                                      |
| [**Interfaz ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accede a un recurso de sombreador.                                      |
| [**Interfaz ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Tiene acceso a una variable de sombreador.                                      |
| [**Interfaz ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Tiene acceso a una cadena.                                               |
| [**Interfaz ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Encapsula uno o varios pases.                                 |
| [**Interfaz ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa métodos para acceder a las variables de efecto.               |
| [**Interfaz ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Accede a un vector.                                               |



 

Hay dos tipos de interfaces en el marco de efecto: interfaces de representación para representar un efecto y interfaces de reflexión para obtener y establecer variables de efecto con la API. Todas las interfaces de reflexión derivan de [**la interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efecto](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
