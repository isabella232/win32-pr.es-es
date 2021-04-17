---
description: En este ejemplo se muestra la descodificación de varios marcos en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de Marcos y la representación de la animación con Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Ejemplo de GIF animado de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653296"
---
# <a name="wic-animated-gif-sample"></a>Ejemplo de GIF animado de WIC

En este ejemplo se muestra la descodificación de varios marcos en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de Marcos y la representación de la animación con Direct2D.

## <a name="requirements"></a>Requisitos

Este ejemplo tiene los siguientes requisitos.

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 7 |
| Windows SDK mínimo | [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Descarga del ejemplo

Este ejemplo está disponible en [GIF animado de WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).

## <a name="building-the-sample"></a>Compilar el ejemplo

### <a name="using-visual-studio-preferred-method"></a>Usar Visual Studio (método preferido)

1. Abra el Explorador de Windows y vaya al directorio.
2. Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.
3. En el menú **Compilar**, seleccione **Compilar solución**. La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.

### <a name="using-the-command-prompt"></a>Uso del símbolo del sistema

Para generar el ejemplo mediante un símbolo del sistema.

1. Abra el símbolo del sistema y navegue hasta el directorio de ejemplo.
2. Escriba `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Ejecución del ejemplo

Una vez iniciada la aplicación, cargue un archivo de imagen con el comando **abrir** del menú **archivo** . Se admite el cambio de tamaño de las ventanas.

## <a name="see-also"></a>Vea también

[Códec de procesamiento de imágenes de Microsoft Windows](-wic-lh.md)

[Guía de programación](-wic-programming-guide.md)

[Referencia](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Ejemplos y ejemplos de código](-wic-samples.md)
