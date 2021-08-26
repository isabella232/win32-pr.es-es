---
title: Ejemplo de comparación de prioridad
description: Muestra cómo usar la Windows con su propia comparación de prioridad, mediante Direct2D para la representación.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafeb2332de02115cbb8af2f2afd69a2fc783be9908a91dbb4e9bb0615876bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008195"
---
# <a name="priority-comparison-sample"></a>Ejemplo de comparación de prioridad

Muestra cómo usar la Windows con su propia comparación de prioridad, mediante Direct2D para la representación.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación                               | Ruta de acceso o dirección URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Kit de desarrollo de software de Windows (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Galería de códigos                           | [Windows Código de ejemplo del Administrador de animaciones](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Después de descargar e instalar el SDK Windows, encontrará los ejemplos en el directorio de instalación. Por ejemplo, si usa la ruta de instalación predeterminada para el SDK de Windows para Windows 7, los ejemplos se instalan en C: Archivos de programa SDK de \\ Microsoft Windows ejemplos de \\ \\ \\ v7.0. \\

## <a name="building-the-sample"></a>Generar el ejemplo

Use uno de los métodos siguientes para compilar el ejemplo.

**Para compilar el ejemplo en el símbolo del sistema**

1.  Abra la ventana símbolo del sistema y vaya al directorio del proyecto PriorityComparison. Por ejemplo, la ruta de instalación predeterminada para este ejemplo es C: Archivos de programa SDK de \\ Microsoft Windows ejemplos de Windows Multimedia \\ \\ \\ v7.0 \\ \\ \\ \\ PriorityComparison.

2.  Ejecute el siguiente comando: **msbuild PriorityComparison.sln**

**Para compilar el ejemplo mediante Microsoft Visual Studio (preferido)**

1.  Abra Windows explorador y vaya al directorio del proyecto PriorityComparison.

2.  Haga doble clic en el icono del archivo PriorityComparison.sln para abrir el proyecto en Visual Studio.

    > [!Note]  
    > La extensión de nombre de archivo .sln no se muestra en la configuración de carpeta predeterminada. En esa situación, se puede identificar por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".

     

3.  En el menú **Compilar**, seleccione **Compilar solución**.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo:

1.  Vaya al directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o Windows Explorer.

2.  Ejecute **PriorityComparison.exe** en el símbolo del sistema o haga doble clic en el icono de PriorityComparison.exe en Windows Explorer.

3.  Las imágenes de ejemplo se cargan desde la biblioteca de imágenes. Cambie el tamaño de la ventana o presione la barra espaciadora y las imágenes se moverán al centro.

4.  Use las teclas de dirección izquierda y derecha para seleccionar imágenes diferentes (cuanto más rápido se presione la tecla, más rápido cambiará la selección).

5.  Use las teclas de flecha arriba y abajo para crear una onda a través de las imágenes (cuanto más rápido se presione la tecla, más rápida será la onda).

 

 




