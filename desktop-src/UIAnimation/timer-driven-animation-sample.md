---
title: Timer-Driven de animación
description: Muestra cómo usar Windows con el temporizador de animación, mientras se usa GDI+ para animar el color de fondo de una ventana.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242126"
---
# <a name="timer-driven-animation-sample"></a>Timer-Driven de animación

Muestra cómo usar Windows con el temporizador de animación, mientras se usa GDI+ para animar el color de fondo de una ventana.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location                               | Ruta de acceso o dirección URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de desarrollo de software de Windows (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galería de códigos                           | [Windows Código de ejemplo del Administrador de animaciones](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Después de descargar e instalar el SDK Windows, encontrará los ejemplos en el directorio de instalación. Por ejemplo, si usa la ruta de instalación predeterminada para el SDK de Windows para Windows 7, los ejemplos se instalan en C: Archivos de programa SDK de \\ Microsoft Windows ejemplos de \\ \\ \\ v7.0. \\

## <a name="building-the-sample"></a>Generar el ejemplo

Use uno de los métodos siguientes para compilar el ejemplo.

**Para compilar el ejemplo en el símbolo del sistema**

1.  Abra la ventana símbolo del sistema y vaya al directorio del proyecto TimerDriven. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: Archivos de programa SDK de Microsoft Windows ejemplos de \\ \\ Windows Multimedia \\ \\ v7.0Contorno de temporizador de \\ \\ \\ \\ implementación.

2.  Ejecute el siguiente comando: **msbuild TimerDriven.sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra Windows explorador y vaya al directorio del proyecto TimerDriven.

2.  Haga doble clic en el icono del archivo TimerDriven.sln para abrir el proyecto en Visual Studio.

    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.

2.  Ejecute **TimerDriven.exe** en el símbolo del sistema o haga doble clic en el icono de TimerDriven.exe en Windows Explorer.

3.  Haga clic en cualquier lugar del área de cliente y el color de fondo de la ventana cambiará a un color aleatorio.

 

 




