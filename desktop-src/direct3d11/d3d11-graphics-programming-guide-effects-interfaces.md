---
title: Interfaces del sistema de efectos (Direct3D 11)
description: El sistema de efectos define varias interfaces para administrar el estado del efecto.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774082"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Interfaces del sistema de efectos (Direct3D 11)

El sistema de efectos define varias interfaces para administrar el estado del efecto. Hay dos tipos de interfaces: las utilizadas por el motor en tiempo de ejecución para representar un efecto e interfaces de reflexión para obtener y establecer las variables de efecto.

-   [Interfaces en tiempo de ejecución de efectos](#effect-runtime-interfaces)
-   [Interfaces de reflexión de efectos](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Interfaces en tiempo de ejecución de efectos

Usar interfaces en tiempo de ejecución para representar un efecto.



| Interfaces en tiempo de ejecución                                       | Descripción                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Colección de uno o más grupos y técnicas para la representación. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Colección de asignaciones de estado.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Colección de uno o más pasos.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Colección de una o más técnicas.                        |



 

## <a name="effect-reflection-interfaces"></a>Interfaces de reflexión de efectos

La reflexión se implementa en el sistema de efectos para admitir el estado del efecto de lectura (y escritura). Hay varias maneras de tener acceso a las variables de efecto.

### <a name="setting-groups-of-effect-state"></a>Configuración de grupos de estado de efecto

Use estas interfaces para obtener y establecer un grupo de estado.



| Interfaces de reflexión                                                          | Descripción                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Obtiene y establece el estado de Blend.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Obtiene y establece el estado de la galería de símbolos de profundidad. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Obtiene y establece el estado del rasterizador.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Obtiene y establece el estado del muestrario.       |



 

### <a name="setting-effect-resources"></a>Configuración de recursos de efectos

Use estas interfaces para obtener y establecer recursos.



| Interfaces de reflexión                                                                        | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Acceder a los datos en un búfer de textura o en un búfer de constantes. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Acceder a los datos en un recurso de estarcido de profundidad.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Acceder a los datos en un destino de representación.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Acceder a los datos de un recurso de sombreador.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Acceder a los datos en una vista de acceso desordenado.            |



 

### <a name="setting-other-effect-variables"></a>Establecer otras variables de efecto

Use estas interfaces para obtener y establecer el estado por el tipo de variable.



| Interfaces de reflexión                                                            | Descripción               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Obtiene una instancia de clase.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Obtiene y establece una interfaz. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Obtiene y establece una matriz.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Obtiene y establece un valor escalar.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Obtiene una variable de sombreador.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Obtiene y establece una cadena.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Obtiene un tipo de variable.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Obtiene y establece un vector.     |



 

Todas las interfaces de reflexión derivan de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

 




