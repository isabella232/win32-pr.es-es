---
title: Información general para desarrolladores
description: Información general para desarrolladores
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Complementos de Windows Media Player, visualizaciones
- complementos, visualizaciones
- visualizaciones, información general para desarrolladores
- visualizaciones personalizadas, información general para desarrolladores
- visualizaciones, controles COM
- visualizaciones personalizadas, controles COM
- visualizaciones, entrada de audio
- visualizaciones personalizadas, entrada de audio
- visualizaciones, salida gráfica
- visualizaciones personalizadas, salida gráfica
- visualizaciones, herramientas de dibujo
- visualizaciones personalizadas, herramientas de dibujo
- visualizaciones, lenguaje de programación
- visualizaciones personalizadas, lenguaje de programación
- visualizaciones, Visual C++
- visualizaciones personalizadas, Visual C++
- visualizaciones, Asistente para complementos
- visualizaciones personalizadas, Asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357382"
---
# <a name="developer-overview"></a>Información general para desarrolladores

Desde el punto de vista del desarrollador, las visualizaciones son programas de software que toman datos de audio proporcionados por Windows Media Player y convierten los datos en gráficos que van a la vista del usuario. Los principales temas que un desarrollador debe comprender para crear una nueva visualización son los siguientes:

## <a name="visualization-packaging"></a>Empaquetado de visualización

Las visualizaciones son controles COM que Windows Media Player usa para convertir las ondas de onda de audio en gráficos animados en Microsoft Windows. Los controles COM se empaquetan como bibliotecas de vínculos dinámicos (dll) de Microsoft Windows y deben estar registrados en el registro de Windows. Cuando se ejecuta Windows Media Player, las visualizaciones personalizadas registradas se cargan y se ven de acuerdo con las instrucciones de la máscara que usa Windows Media Player.

## <a name="audio-input"></a>Entrada de audio

Windows Media Player proporciona el código con instantáneas de los datos de frecuencia de audio y de forma de onda a intervalos de tiempo medidos en fracciones de segundo. El intervalo de instantánea está determinado internamente por el Media Player de Windows.

## <a name="graphical-output"></a>Salida gráfica

La salida gráfica de la visualización es un contexto de dispositivo de Microsoft Windows. Se trata de una superficie de dibujo estándar de Windows que se puede dibujar cada vez que se proporciona una instantánea de audio. Toda la tecnología de Windows en segundo plano se encarga de usted. Solo tiene que dibujar en el contexto del dispositivo con los datos de audio proporcionados.

## <a name="drawing-tools"></a>Herramientas de dibujo

Puede dibujar en el contexto del dispositivo con las funciones estándar de Microsoft Windows Interfaz de dispositivo gráfico (GDI), usando lápices y pinceles para crear diseños modificados por los datos de audio que proporciona Windows Media Player. GDI proporciona un amplio conjunto de herramientas de dibujo que pueden crear muchos tipos de efectos visuales.

## <a name="programming-language"></a>Lenguaje de programación

Microsoft Visual C++ 6,0 y versiones posteriores es el único idioma admitido para crear visualizaciones personalizadas.

## <a name="plug-in-wizard"></a>Asistente para complementos

Windows Media Player proporciona un asistente COM que se puede Agregar a Visual C++ que generará el código subyacente necesario para la visualización. No solo se proporcionan todos los archivos de código fuente, pero se genera una máscara de ejemplo para facilitar la prueba de la visualización. El código generado crea una visualización similar a las barras, con dos valores preestablecidos. Después, puede modificar el código para crear su propia visualización. También se genera un archivo de registro para registrar la visualización de forma que Windows Media Player pueda cargarla.

En el siguiente tema se describe cómo el código de visualización procesa los datos de audio:

-   [Flujo de control](flow-of-control.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las visualizaciones personalizadas**](about-custom-visualizations.md)
</dt> </dl>

 

 




