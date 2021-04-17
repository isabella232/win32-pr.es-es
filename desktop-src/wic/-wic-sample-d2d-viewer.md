---
description: En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar un archivo de imagen y Direct2D para representar la imagen en la pantalla.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visor de imágenes WIC con el ejemplo de Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653295"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>Visor de imágenes WIC con el ejemplo de Direct2D

En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar un archivo de imagen y Direct2D para representar la imagen en la pantalla.

## <a name="requirements"></a>Requisitos

Este ejemplo tiene los siguientes requisitos.

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows Vista |
| Windows SDK mínimo | [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Descarga del ejemplo

Este ejemplo está disponible en el [visor de WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).

## <a name="building-the-sample"></a>Compilar el ejemplo

### <a name="using-visual-studio-preferred-method"></a>Usar Visual Studio (método preferido)

1. Abra el Explorador de Windows y vaya al directorio.
2. Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.
3. En el menú **Compilar**, seleccione **Compilar solución**. La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.

### <a name="using-the-command-prompt"></a>Uso del símbolo del sistema

Para compilar el ejemplo mediante un símbolo del sistema:

1. Abra una ventana del símbolo del sistema y navegue hasta el directorio de ejemplo.
2. Escriba `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>Ejecución del ejemplo

Una vez iniciada la aplicación, cargue un archivo de imagen con el comando **abrir** del menú **archivo** .

## <a name="see-also"></a>Vea también

[Códec de procesamiento de imágenes de Microsoft Windows](-wic-lh.md)

[Guía de programación](-wic-programming-guide.md)

[Referencia](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Ejemplos y ejemplos de código](-wic-samples.md)
