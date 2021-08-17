---
title: Application-Driven de animación
description: Muestra Windows animación en la configuración controlada por la aplicación mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfbb5ce71ddeff6a37c2d872e0e1e93fdc58cde9fcc8359560d9d386ba7a0834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137378"
---
# <a name="application-driven-animation-sample"></a>Application-Driven de animación

Muestra Windows animación en la configuración controlada por la aplicación mediante Direct2D para animar el color de fondo de una ventana y sincronizar con la frecuencia de actualización.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación                               | Ruta de acceso o dirección URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de desarrollo de software de Windows (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galería de códigos                           | [Windows Código de ejemplo del administrador de animaciones](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Después de descargar e instalar el SDK Windows, encontrará los ejemplos en el directorio de instalación. Por ejemplo, si usa la ruta de instalación predeterminada para el SDK de Windows para Windows 7, los ejemplos se instalan en C: Archivos de programa SDK de \\ Microsoft Windows ejemplos de \\ \\ \\ v7.0. \\

## <a name="building-the-sample"></a>Generar el ejemplo

Use uno de los métodos siguientes para compilar el ejemplo.

**Para compilar el ejemplo en el símbolo del sistema**

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto de AppDriven. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: Archivos de programa SDK de Microsoft Windows ejemplos \\ \\ de Windows Multimedia \\ \\ v7.0Adriveción \\ de aplicaciones \\ \\ \\ móviles.

2.  Ejecute el siguiente comando: **msbuild AppDriven.sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida)**

1.  Abra Windows Explorador de aplicaciones y vaya al directorio del proyecto de AppDriven.

2.  Haga doble clic en el icono del archivo AppDriven.sln para abrir el proyecto en Visual Studio.

    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorador.

2.  Ejecute **AppDriven.exe** en el símbolo del sistema o haga doble clic en el icono de AppDriven.exe en Windows Explorer.

3.  Haga clic en cualquier parte del área de cliente y el color de fondo de la ventana cambiará a un color aleatorio.

 

 




