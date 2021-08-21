---
description: En este ejemplo se muestra el uso de Windows Imaging Component (WIC) para descodificar una imagen codificada con niveles progresivas.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Ejemplo de decodación progresiva de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 26e26670aad4e3aeed8fca167d77ba6ad36b931d738fccf9717c6e119bf943a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032032"
---
# <a name="wic-progressive-decoding-sample"></a>Ejemplo de decodación progresiva de WIC

En este ejemplo se muestra el uso de Windows Imaging Component (WIC) para descodificar una imagen codificada con niveles progresivas. En este ejemplo se usa Direct2D para representar los distintos niveles progresivas en la pantalla.

## <a name="requirements"></a>Requisitos

Este ejemplo tiene los siguientes requisitos.

| Requisito | Valor |
|-|
| Cliente mínimo compatible | Windows 7 |
| SDK Windows mínimo | [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Descarga del ejemplo

Este ejemplo está disponible en [codificación progresiva de WIC.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding)

## <a name="building-the-sample"></a>Compilar el ejemplo

### <a name="using-visual-studio-preferred-method"></a>Usar Visual Studio (método preferido)

1. Abra el Explorador de Windows y vaya al directorio.
2. Haga doble clic en el icono del archivo .sln (solución) para abrir el archivo en Visual Studio.
3. En el menú Compilar, seleccione Compilar solución. La aplicación se compilará en el directorio \\ de depuración o \\ versión predeterminado.

### <a name="using-the-command-prompt"></a>Uso del símbolo del sistema

Para compilar el ejemplo mediante el símbolo del sistema.

1. Abra el símbolo del sistema y vaya al directorio de ejemplo.
2. Escriba `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Ejecución del ejemplo

Una vez iniciada la aplicación, cargue un archivo de imagen a través del menú de apertura de archivos. Al cargar, el nivel progresiva predeterminado se establece en 0. Puede navegar a diferentes niveles progresivas a través del menú o la tecla Arriba/Abajo. El texto de nivel progresiva actual se muestra en la barra de estado de la ventana principal. Se admite el tamaño de ventana.

> [!NOTE]
> La descodificación progresiva solo está disponible para las imágenes que se han codificado progresivamente. La imagen proporcionada con este ejemplo se ha codificado progresivamente.

## <a name="see-also"></a>Vea también

[Códec microsoft Windows imaging](-wic-lh.md)

[Guía de programación](-wic-programming-guide.md)

[Referencia](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Ejemplos y ejemplos de código](-wic-samples.md)

[Introducción a la decodificación progresiva](-wic-progressive-decoding.md)
