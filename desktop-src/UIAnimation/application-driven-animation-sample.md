---
title: Ejemplo de animación Application-Driven
description: Muestra la animación de Windows en la configuración controlada por aplicaciones mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "105685688"
---
# <a name="application-driven-animation-sample"></a>Ejemplo de animación Application-Driven

Muestra la animación de Windows en la configuración controlada por aplicaciones mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location                               | Ruta de acceso/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de desarrollo de software de Windows (SDK) | [Kit de desarrollo de software de Microsoft Windows 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galería de códigos                           | [Código de ejemplo del administrador de animaciones de Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Después de haber descargado e instalado el Windows SDK, encontrará los ejemplos en el directorio de instalación. Por ejemplo, si usa la ruta de instalación predeterminada para el Windows SDK para Windows 7, los ejemplos se instalan en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples.

## <a name="building-the-sample"></a>Generar el ejemplo

Use uno de los métodos siguientes para compilar el ejemplo.

**Para generar el ejemplo en el símbolo del sistema**

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto AppDriven. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ AppDriven.

2.  Ejecute el siguiente comando: **msbuild AppDriven. sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto AppDriven.

2.  Haga doble clic en el icono del archivo AppDriven. sln para abrir el proyecto en Visual Studio.

    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.

2.  Ejecute **AppDriven.exe** en el símbolo del sistema o haga doble clic en el icono de AppDriven.exe en el explorador de Windows.

3.  Haga clic en cualquier parte del área cliente y el color de fondo de la ventana cambiará a un color aleatorio.

 

 




