---
title: Ejemplo de comparación de prioridades
description: Muestra cómo usar la animación de Windows con su propia comparación de prioridad mediante Direct2D para la representación.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104149149"
---
# <a name="priority-comparison-sample"></a>Ejemplo de comparación de prioridades

Muestra cómo usar la animación de Windows con su propia comparación de prioridad mediante Direct2D para la representación.

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

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto PriorityComparison. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ WindowsAnimation \\ PriorityComparison.

2.  Ejecute el siguiente comando: **msbuild PriorityComparison. sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto PriorityComparison.

2.  Haga doble clic en el icono del archivo PriorityComparison. sln para abrir el proyecto en Visual Studio.

    > [!Note]  
    > La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada. En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **compilar** , seleccione **compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.

2.  Ejecute **PriorityComparison.exe** en el símbolo del sistema o haga doble clic en el icono de PriorityComparison.exe en el explorador de Windows.

3.  Las imágenes de ejemplo se cargan desde la biblioteca de imágenes. Cambie el tamaño de la ventana o presione la barra espaciadora y las imágenes se moverán al centro.

4.  Use las teclas de flecha izquierda y derecha para seleccionar distintas imágenes (cuanto más rápido se presiona la tecla más rápido cambiará la selección).

5.  Use las teclas de flecha arriba y abajo para crear una onda a través de las imágenes (cuanto más rápido se presiona la tecla, más rápida es la onda).

 

 




