---
description: 'Esta sección contiene información sobre las siguientes interfaces del sistema de efecto:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Interfaces de efectos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807160"
---
# <a name="effect-interfaces-direct3d-10"></a>Interfaces de efectos (Direct3D 10)

Esta sección contiene información sobre las siguientes interfaces del sistema de efecto:



| Interfaces                                                                                     | Descripción                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Interfaz ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Accede al estado de Blend.                                            |
| [**Interfaz ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Accede a un búfer de textura o a un búfer de constantes.                  |
| [**Interfaz ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Obtiene acceso al estado de la galería de símbolos de profundidad.                                    |
| [**Interfaz ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Obtiene acceso a una vista de galería de símbolos de profundidad.                                   |
| [**Interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Encapsula el estado de la canalización en una o más técnicas de representación. |
| [**Interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Métodos implementados por el usuario para leer archivos de inclusión.              |
| [**Interfaz ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Obtiene acceso a una matriz.                                               |
| [**Interfaz ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Encapsula el estado del efecto en un paso.                             |
| [**Interfaz ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Identifica las variables de efectos compartidos.                              |
| [**Interfaz ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Obtiene acceso al estado del rasterizador.                                       |
| [**Interfaz ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Obtiene acceso a un destino de representación.                                        |
| [**Interfaz ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Obtiene acceso al estado de muestra.                                          |
| [**Interfaz ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Obtiene acceso a una variable escalar.                                      |
| [**Interfaz ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Accede a un recurso de sombreador.                                      |
| [**Interfaz ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Obtiene acceso a una variable de sombreador.                                      |
| [**Interfaz ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Obtiene acceso a una cadena.                                               |
| [**Interfaz ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Encapsula una o varias fases.                                 |
| [**Interfaz ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Implementa los métodos para tener acceso a las variables de efecto.               |
| [**Interfaz ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Obtiene acceso a un vector.                                               |



 

Hay dos tipos de interfaces en el marco de trabajo de efecto: interfaces de representación para representar un efecto e interfaces de reflexión para obtener y establecer las variables de efecto con la API. Todas las interfaces de reflexión derivan de la [**interfaz ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efectos](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 
