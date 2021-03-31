---
title: Administrador de animaciones de Windows
description: El administrador de animaciones de Windows (animación de Windows) permite una animación enriquecida de elementos de la interfaz de usuario.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animación de Windows animación de Windows, portal
- Animación de Windows del administrador de animaciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995377"
---
# <a name="windows-animation-manager"></a>Administrador de animaciones de Windows

## <a name="purpose"></a>Propósito

El administrador de animaciones de Windows (animación de Windows) permite una animación enriquecida de elementos de la interfaz de usuario. Está diseñado para simplificar el proceso de agregar animación a la interfaz de usuario de una aplicación y permitir a los desarrolladores implementar animaciones que son suaves, naturales e interactivas.

El marco de animaciones administra la programación y la ejecución de animaciones. Proporciona una biblioteca de funciones matemáticas útiles para especificar el comportamiento de un elemento de la interfaz de usuario a lo largo del tiempo, y también permite a los desarrolladores implementar funciones personalizadas que proporcionan comportamientos adicionales.

La animación de Windows no realiza la representación; se puede usar con cualquier plataforma de gráficos, como Direct2D, Direct3D o GDI+.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Guía de desarrollo de animaciones de Windows](windows-animation-developer-guide.md)<br/> | La guía del Desarrollador proporciona información general sobre la animación de Windows y proporciona código de ejemplo que abarca las tareas de animación básicas.<br/>          |
| [Referencia de animación de Windows](windows-animation-reference.md)<br/>               | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el administrador de animaciones de Windows.<br/>                           |
| [Ejemplos de animación de Windows](windows-animation-samples.md)<br/>                   | Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación del administrador de animaciones de Windows. <br/> |
| [Glosario de animaciones de Windows](-ui-animation-glossary.md)<br/>                     | Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan el administrador de animaciones de Windows.<br/>                               |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows Animation está diseñado para su uso por parte de desarrolladores de C/C++ con experiencia que están familiarizados con COM, los conceptos de programación de la interfaz de usuario y los conceptos de animación generales.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

El administrador de animaciones de Windows se presentó en Windows 7.

Las aplicaciones que requieren compatibilidad con el administrador de animaciones de Windows en Windows Vista pueden utilizar la actualización de la plataforma para Windows Vista. Las aplicaciones que requieren la actualización de la plataforma para Windows Vista pueden tener Windows Update comprobar que está instalada, o bien descargarlas e instalarlas en segundo plano. Para obtener más información, vea acerca de la [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Recursos adicionales

-   [Información general sobre animaciones de Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vídeo)
-   [Dentro de Windows 7: tutorial y análisis en profundidad del administrador de animaciones](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vídeo)
-   [Animación de Windows: temas avanzados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)
-   [Código de ejemplo del administrador de animaciones de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Temas relacionados

[Información general sobre animaciones (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)