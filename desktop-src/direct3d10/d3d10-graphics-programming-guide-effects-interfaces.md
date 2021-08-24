---
description: 'El sistema de efectos define varias interfaces para administrar el estado del efecto. Hay dos tipos de interfaces: las usadas por el tiempo de ejecución para representar interfaces de efecto y reflexión para obtener y establecer variables de efecto.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Interfaces del sistema de efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5d640b31d0d1db9ac9b58ed166b45acff762b30edc0e71f1d7138b5818b3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128397"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Interfaces del sistema de efecto (Direct3D 10)

El sistema de efectos define varias interfaces para administrar el estado del efecto. Hay dos tipos de interfaces: las usadas por el tiempo de ejecución para representar interfaces de efecto y reflexión para obtener y establecer variables de efecto.

-   [Interfaces en tiempo de ejecución de efecto](#effect-runtime-interfaces)
-   [Interfaces de reflexión de efectos](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces en tiempo de ejecución de efecto

Use interfaces en tiempo de ejecución para representar un efecto.



| Interfaces en tiempo de ejecución                                               | Descripción                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Colección de una o varias técnicas para la representación.                  |
| [**Interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Interfaz para agregar comportamientos personalizados al leer archivos de incluyen. |
| [**Interfaz ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Colección de asignaciones de estado.                                   |
| [**Interfaz ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Cree una ubicación de memoria para que las variables se compartan entre los efectos. |
| [**Interfaz ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Colección de uno o varios pases.                                  |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexión de efectos

La reflexión se implementa en el sistema de efectos para admitir el estado del efecto de lectura (y escritura). Hay varias maneras de acceder a las variables de efecto.

### <a name="setting-groups-of-effect-state"></a>Establecer grupos de estado de efecto

Use estas interfaces para obtener y establecer un grupo de estado.



| Interfaces de reflexión                                                                  | Descripción                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Interfaz ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Obtiene y establece el estado de blend.         |
| [**Interfaz ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Obtiene y establece el estado de la galería de símbolos de profundidad. |
| [**Interfaz ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Obtiene y establece el estado del rasterizador.    |
| [**Interfaz ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Obtiene y establece el estado del sampler.       |



 

### <a name="setting-effect-resources"></a>Establecer recursos de efecto

Use estas interfaces para obtener y establecer recursos.



| Interfaces de reflexión                                                                          | Descripción                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Interfaz ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Acceso a datos en un búfer de textura o búfer constante. |
| [**Interfaz ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Acceso a datos en un recurso de galería de símbolos de profundidad.            |
| [**Interfaz ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Acceso a datos en un destino de representación.                     |
| [**Interfaz ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Acceso a datos en un recurso de sombreador.                   |



 

### <a name="setting-other-effect-variables"></a>Establecer otras variables de efecto

Use estas interfaces para obtener y establecer el estado según el tipo de variable.



| Interfaces de reflexión                                                      | Descripción                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Interfaz ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Obtiene y establece una matriz.          |
| [**Interfaz ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Obtiene y establece un valor escalar.          |
| [**Interfaz ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Obtiene y establece una variable de sombreador. |
| [**Interfaz ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Obtiene y establece una cadena.          |
| [**Interfaz ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Obtiene un tipo de variable.           |
| [**Interfaz ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Obtiene y establece un vector.          |



 

Todas las interfaces de reflexión derivan de la interfaz [**ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
