---
title: Ejemplo de interpolador personalizado
description: Muestra cómo usar la animación de Windows con su propio interpolador personalizado, con Direct2D usado para la representación.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104149150"
---
# <a name="custom-interpolator-sample"></a>Ejemplo de interpolador personalizado

Muestra cómo usar la animación de Windows con su propio interpolador personalizado, con Direct2D usado para la representación. Las imágenes de ejemplo se cargan desde la biblioteca de imágenes.

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

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto CustomInterpolator. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ CustomInterpolator

2.  Ejecute el siguiente comando: **msbuild CustomInterpolator. sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto CustomInterpolator.

    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

2.  Haga doble clic en el icono del archivo CustomInterpolator. sln para abrir el proyecto en Visual Studio.

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.

2.  Ejecute **CustomInterpolator.exe** en el símbolo del sistema o haga doble clic en el icono de CustomInterpolator.exe en el explorador de Windows.
3.  Cambie el tamaño de la ventana o presione la barra espaciadora, y las imágenes se organizarán de forma aleatoria en el centro del área cliente.

4.  Presione la flecha arriba o abajo para que las imágenes se aceleren hacia la parte superior o inferior del área cliente.

 

 




