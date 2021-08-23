---
title: Ejemplo de interpolador personalizado
description: Muestra cómo usar Windows animación con su propio interpolador personalizado, con Direct2D usado para la representación.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c801822bd50eebe9f405cad00bc8ffcd7ac2d611924a3ff0bae91d30bc9f249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999705"
---
# <a name="custom-interpolator-sample"></a>Ejemplo de interpolador personalizado

Muestra cómo usar Windows animación con su propio interpolador personalizado, con Direct2D usado para la representación. Las imágenes de ejemplo se cargan desde la biblioteca de imágenes.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación                               | Ruta de acceso o dirección URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de desarrollo de software de Windows (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galería de códigos                           | [Windows Código de ejemplo del administrador de animaciones](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Después de descargar e instalar el SDK de Windows, encontrará los ejemplos en el directorio de instalación. Por ejemplo, si usa la ruta de instalación predeterminada para el SDK de Windows para Windows 7, los ejemplos se instalan en C: Archivos de programa SDK de \\ \\ Microsoft Windows ejemplos \\ \\ v7.0. \\

## <a name="building-the-sample"></a>Generar el ejemplo

Use uno de los métodos siguientes para compilar el ejemplo.

**Para compilar el ejemplo en el símbolo del sistema**

1.  Abra la ventana del símbolo del sistema y vaya al directorio del proyecto CustomInterpolator. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: Archivos de programa SDK de Microsoft Windows ejemplos \\ \\ de Windows Multimedia \\ \\ v7.0Animation \\ \\ \\ \\ CustomInterpolator

2.  Ejecute el siguiente comando: **msbuild CustomInterpolator.sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (opción preferida)**

1.  Abra Windows Explorador de aplicaciones y vaya al directorio del proyecto CustomInterpolator.

    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

2.  Haga doble clic en el icono del archivo CustomInterpolator.sln para abrir el proyecto en Visual Studio.

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Windows Explorador.

2.  Ejecute **CustomInterpolator.exe** en el símbolo del sistema o haga doble clic en el icono de CustomInterpolator.exe en Windows Explorer.
3.  Cambie el tamaño de la ventana o presione la barra espaciadora y las imágenes se organizarán aleatoriamente en el centro del área de cliente.

4.  Presione la flecha arriba o abajo y las imágenes se acelerarán hacia la parte superior o inferior del área cliente.

 

 




