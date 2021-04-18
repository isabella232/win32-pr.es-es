---
description: En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar una imagen codificada con niveles progresivos.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Ejemplo de descodificación progresiva de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718593"
---
# <a name="wic-progressive-decoding-sample"></a>Ejemplo de descodificación progresiva de WIC

En este ejemplo se muestra el uso del componente de creación de imágenes de Windows (WIC) para descodificar una imagen codificada con niveles progresivos. En este ejemplo se usa Direct2D para representar los distintos niveles progresivos en la pantalla.

## <a name="requirements"></a>Requisitos

Este ejemplo tiene los siguientes requisitos.

| Requisito | Value |
|-|
| Cliente mínimo compatible | Windows 7 |
| Windows SDK mínimo | [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Descarga del ejemplo

Este ejemplo está disponible en la [codificación progresiva de WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).

## <a name="building-the-sample"></a>Compilar el ejemplo

### <a name="using-visual-studio-preferred-method"></a>Usar Visual Studio (método preferido)

1. Abra el Explorador de Windows y vaya al directorio.
2. Haga doble clic en el icono del archivo. sln (solución) para abrir el archivo en Visual Studio.
3. En el menú Compilar, seleccione Compilar solución. La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.

### <a name="using-the-command-prompt"></a>Uso del símbolo del sistema

Para compilar el ejemplo mediante el símbolo del sistema.

1. Abra el símbolo del sistema y navegue hasta el directorio de ejemplo.
2. Escriba `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Ejecución del ejemplo

Una vez iniciada la aplicación, cargue un archivo de imagen a través del menú archivo abierto. Al cargar, el nivel progresivo predeterminado se establece en 0. Puede desplazarse a distintos niveles progresivos, ya sea a través del menú o de la tecla arriba o abajo. El texto de nivel progresivo actual se muestra en la barra de estado de la ventana principal. Se admite el cambio de tamaño de las ventanas.

> [!NOTE]
> La descodificación progresiva solo está disponible para las imágenes que se han codificado progresivamente. La imagen proporcionada con este ejemplo se ha codificado progresivamente.

## <a name="see-also"></a>Vea también

[Códec de procesamiento de imágenes de Microsoft Windows](-wic-lh.md)

[Guía de programación](-wic-programming-guide.md)

[Referencia](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Ejemplos y ejemplos de código](-wic-samples.md)

[Información general sobre descodificación progresiva](-wic-progressive-decoding.md)
