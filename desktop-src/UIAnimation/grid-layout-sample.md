---
title: Ejemplo de diseño de cuadrícula
description: Muestra cómo usar Windows animación mediante Direct2D para animar una cuadrícula de imágenes.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264852"
---
# <a name="grid-layout-sample"></a>Ejemplo de diseño de cuadrícula

Muestra cómo usar Windows animación mediante Direct2D para animar una cuadrícula de imágenes.

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

1.  Abra la ventana símbolo del sistema y vaya al directorio del proyecto GridLayout. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: Archivos de programa SDK de \\ \\ Microsoft Windows \\ \\ v7.0 \\ Ejemplos de Windows \\ \\ MultimediaAnimation \\ GridLayout

2.  Ejecute el siguiente comando: **msbuild GridLayout.sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra Windows Explorer y vaya al directorio del proyecto GridLayout.

    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

2.  Haga doble clic en el icono del archivo GridLayout.sln para abrir el proyecto en Visual Studio.

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.

2.  Ejecute **GridLayout.exe** en el símbolo del sistema o haga doble clic en el icono de GridLayout.exe en Windows Explorer.

3.  Las imágenes de ejemplo se cargan desde la biblioteca de imágenes. Cambie el tamaño de la ventana y las imágenes se organizarán en una cuadrícula.

 

 




