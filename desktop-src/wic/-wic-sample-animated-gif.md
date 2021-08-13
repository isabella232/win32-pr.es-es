---
description: En este ejemplo se muestra la decodación de varios fotogramas en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de fotogramas y la representación de la animación con Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Ejemplo de GIF animado de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 925beb45b58bdecb7d12505a9d2067cbcb9e6fbf1867786286f18333fea986e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709619"
---
# <a name="wic-animated-gif-sample"></a>Ejemplo de GIF animado de WIC

En este ejemplo se muestra la decodación de varios fotogramas en un archivo GIF, la lectura de los metadatos adecuados para cada fotograma, la composición de fotogramas y la representación de la animación con Direct2D.

## <a name="requirements"></a>Requisitos

Este ejemplo tiene los siguientes requisitos.

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 7 |
| SDK Windows mínimo | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Descarga del ejemplo

Este ejemplo está disponible en [EL GIF animado de WIC.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif)

## <a name="building-the-sample"></a>Compilar el ejemplo

### <a name="using-visual-studio-preferred-method"></a>Usar Visual Studio (método preferido)

1. Abra el Explorador de Windows y vaya al directorio.
2. Haga doble clic en el icono del archivo .sln (solución) para abrir el archivo en Visual Studio.
3. En el menú **Compilar**, seleccione **Compilar solución**. La aplicación se compilará en el directorio \\ debug o \\ release predeterminado.

### <a name="using-the-command-prompt"></a>Uso del símbolo del sistema

Para compilar el ejemplo mediante un símbolo del sistema.

1. Abra el símbolo del sistema y vaya al directorio de ejemplo.
2. Escriba `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Ejecución del ejemplo

Una vez iniciada la aplicación, cargue un archivo de imagen mediante **el** comando Abrir del **menú** Archivo. Se admite el tamaño de ventana.

## <a name="see-also"></a>Vea también

[Códec microsoft Windows imaging](-wic-lh.md)

[Guía de programación](-wic-programming-guide.md)

[Referencia](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Ejemplos y ejemplos de código](-wic-samples.md)
