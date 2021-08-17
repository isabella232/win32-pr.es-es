---
title: Windows Administrador de animaciones
description: El administrador Windows animación (Windows animación) permite una animación enriquecente de elementos de la interfaz de usuario.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows Animation Windows Animation ,portal
- Windows Animation Manager Windows Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e6a8f81fbef55525eff04df52a31f8ee942707c354697658ee0ba01647d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755619"
---
# <a name="windows-animation-manager"></a>Windows Administrador de animaciones

## <a name="purpose"></a>Propósito

El administrador Windows animación (Windows animación) permite una animación enriquecente de elementos de la interfaz de usuario. Está diseñado para simplificar el proceso de agregar animación a la interfaz de usuario de una aplicación y para permitir a los desarrolladores implementar animaciones que sean fluidas, naturales e interactivas.

El marco de animación administra la programación y ejecución de animaciones. Proporciona una biblioteca de funciones matemáticas útiles para especificar el comportamiento de un elemento de la interfaz de usuario a lo largo del tiempo y también permite a los desarrolladores implementar funciones personalizadas que proporcionan comportamientos adicionales.

Windows La animación no realiza la representación; se puede usar con cualquier plataforma de gráficos, incluidos Direct2D, Direct3D o GDI+.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Guía de desarrollo de animaciones](windows-animation-developer-guide.md)<br/> | La guía para desarrolladores proporciona información general sobre Windows animación y proporciona código de ejemplo que cubre las tareas básicas de animación.<br/>          |
| [Windows Referencia de animación](windows-animation-reference.md)<br/>               | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para el administrador Windows animación.<br/>                           |
| [Windows Ejemplos de animación](windows-animation-samples.md)<br/>                   | Los temas contenidos en esta sección proporcionan detalles sobre los ejemplos de código que admiten la documentación Windows Animation Manager. <br/> |
| [Windows Glosario de animación](-ui-animation-glossary.md)<br/>                     | Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan Windows Animation Manager.<br/>                               |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows La animación está diseñada para su uso por desarrolladores experimentados de C/C++ que están familiarizados con COM, los conceptos de programación de la interfaz de usuario y los conceptos generales de animación.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

El Windows Animation Manager se introdujo en Windows 7.

Las aplicaciones que requieren compatibilidad con Windows Animation Manager en Windows Vista pueden usar la actualización de plataforma para Windows Vista. Las aplicaciones que requieren La actualización de plataforma para Windows Vista pueden hacer que Windows Update compruebe que está instalada, o bien descargarla e instalarla en segundo plano de lo contrario. Para obtener más información, vea [Acerca de la actualización de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Recursos adicionales

-   [Windows información general sobre animación de animación de animación](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) de animación (vídeo)
-   [Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (Tutorial)
-   [Windows animación: temas avanzados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)
-   [Windows Código de ejemplo del administrador de animaciones](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Temas relacionados

[Información general sobre animaciones (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)