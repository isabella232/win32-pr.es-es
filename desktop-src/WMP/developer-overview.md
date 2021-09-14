---
title: Información general para desarrolladores
description: Información general para desarrolladores
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Reproductor de Windows Media complementos, visualizaciones
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
- visualizaciones, asistente para complementos
- visualizaciones personalizadas, asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068471"
---
# <a name="developer-overview"></a>Información general para desarrolladores

Desde el punto de vista del desarrollador, las visualizaciones son programas de software que toman los datos de audio proporcionados por Reproductor de Windows Media y convierten los datos en gráficos que van a complacer al usuario. Los temas principales que un desarrollador debe comprender para crear una nueva visualización son los siguientes:

## <a name="visualization-packaging"></a>Empaquetado de visualización

Las visualizaciones son controles COM que Reproductor de Windows Media para convertir formas de onda de audio en gráficos animados en Microsoft Windows. Los controles COM se empaquetan como bibliotecas de vínculos dinámicos (DLL) de Microsoft Windows y deben estar registrados en el Windows web. Cuando Reproductor de Windows Media, las visualizaciones personalizadas registradas se cargan y se ven de acuerdo con las instrucciones de la máscara que Reproductor de Windows Media está usando.

## <a name="audio-input"></a>Entrada de audio

Reproductor de Windows Media proporciona al código instantáneas de datos de frecuencia de audio y forma de onda a intervalos de tiempo medidos en fracciones de segundo. El intervalo de instantáneas viene determinado internamente por el Reproductor de Windows Media.

## <a name="graphical-output"></a>Salida gráfica

La salida gráfica de la visualización es un contexto Windows de dispositivo de Microsoft. Se trata de un Windows superficie de dibujo que se puede dibujar cada vez que se proporciona una instantánea de audio. Toda la información Windows la tecnología se encarga de usted. Solo tiene que dibujar en el contexto del dispositivo con los datos de audio proporcionados.

## <a name="drawing-tools"></a>Herramientas de dibujo

Puede dibujar en el contexto del dispositivo con funciones estándar de Microsoft Windows Interfaz de dispositivo gráfico (GDI), mediante lápices y pinceles para crear diseños modificados por los datos de audio proporcionados por Reproductor de Windows Media. GDI proporciona un amplio conjunto de herramientas de dibujo que pueden crear muchos tipos de efectos visuales.

## <a name="programming-language"></a>Lenguaje de programación

Microsoft Visual C++ 6.0 y versiones posteriores es el único lenguaje admitido para crear visualizaciones personalizadas.

## <a name="plug-in-wizard"></a>Asistente para complementos

Reproductor de Windows Media proporciona un asistente COM que puede agregar a Visual C++ que generará el código subyacente necesario para la visualización. No solo se proporcionan todos los archivos de código fuente, sino que se genera una máscara de ejemplo para facilitar la prueba de la visualización. El código generado crea una visualización similar a Barras, con dos valores preestablecidos. A continuación, puede modificar el código para crear su propia visualización. También se genera un archivo del Registro para registrar la visualización para que Reproductor de Windows Media pueda cargarlo.

En el tema siguiente se describe cómo procesa el código de visualización los datos de audio:

-   [Flow de control](flow-of-control.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las visualizaciones personalizadas**](about-custom-visualizations.md)
</dt> </dl>

 

 




