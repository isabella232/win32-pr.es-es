---
title: Interfaces del sistema de efecto (Direct3D 11)
description: El sistema de efectos define varias interfaces para administrar el estado del efecto.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361296"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Interfaces del sistema de efecto (Direct3D 11)

El sistema de efectos define varias interfaces para administrar el estado del efecto. Hay dos tipos de interfaces: las usadas por el tiempo de ejecución para representar interfaces de efecto y reflexión para obtener y establecer variables de efecto.

-   [Interfaces de tiempo de ejecución de efecto](#effect-runtime-interfaces)
-   [Interfaces de reflexión de efectos](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces en tiempo de ejecución de efecto

Use interfaces en tiempo de ejecución para representar un efecto.



| Interfaces en tiempo de ejecución                                       | Descripción                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Colección de uno o varios grupos y técnicas para la representación. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Colección de asignaciones de estado.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Colección de uno o varios pases.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Colección de una o varias técnicas.                        |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexión de efectos

La reflexión se implementa en el sistema de efectos para admitir el estado del efecto de lectura (y escritura). Hay varias maneras de acceder a las variables de efecto.

### <a name="setting-groups-of-effect-state"></a>Establecer grupos de estado de efecto

Use estas interfaces para obtener y establecer un grupo de estado.



| Interfaces de reflexión                                                          | Descripción                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Obtiene y establece el estado de blend.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Obtiene y establece el estado de la galería de símbolos de profundidad. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Obtiene y establece el estado del rasterizador.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Obtiene y establece el estado del sampler.       |



 

### <a name="setting-effect-resources"></a>Establecer recursos de efecto

Use estas interfaces para obtener y establecer recursos.



| Interfaces de reflexión                                                                        | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Acceso a datos en un búfer de textura o búfer constante. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Acceso a datos en un recurso de galería de símbolos de profundidad.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Acceso a datos en un destino de representación.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Acceso a datos en un recurso de sombreador.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Acceso a datos en una vista de acceso desordenado.            |



 

### <a name="setting-other-effect-variables"></a>Establecer otras variables de efecto

Use estas interfaces para obtener y establecer el estado según el tipo de variable.



| Interfaces de reflexión                                                            | Descripción               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Obtenga una instancia de clase.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Obtiene y establece una interfaz. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Obtiene y establece una matriz.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Obtiene y establece un valor escalar.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Obtiene una variable de sombreador.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Obtiene y establece una cadena.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Obtiene un tipo de variable.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Obtiene y establece un vector.     |



 

Todas las interfaces de reflexión [**derivan de ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

 




