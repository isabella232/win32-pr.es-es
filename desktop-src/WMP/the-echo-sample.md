---
title: El ejemplo de eco
description: El ejemplo de eco
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Reproductor de Windows Media complementos, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- complementos de procesamiento de señales digitales, información general de ejemplo de eco
- Complementos de DSP, información general de ejemplo de eco
- guía de programación, complementos DE DSP
- samples,DSP plug-ins
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f2dfe6a59257b8a16dc31a5b4cb751d649cd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264740"
---
# <a name="the-echo-sample"></a>El ejemplo de eco

El Reproductor de Windows Media complemento de Reproductor de Windows Media puede crear un proyecto de complemento DSP para Microsoft Visual C++. El código predeterminado generado por el asistente permite al usuario proporcionar un factor de escala entre 0 y 1, que el programa usa como multiplicador para los ejemplos de audio. Se trata de una implementación muy sencilla que puede estudiar para comprender Reproductor de Windows Media interactúa con los complementos de DSP. La información de la sección denominada [About DSP Plug-ins](about-dsp-plug-ins.md) (Acerca de los complementos de DSP) puede ayudarle a comprender la implementación predeterminada.

El ejemplo descrito en esta sección es un poco más complejo. Este ejemplo permite al usuario especificar un tiempo de retraso, en milisegundos, y un nivel de efecto. El código usa estos valores para generar un efecto de eco al reproducir archivos que contienen audio de codificación de pulsación (PCM). Muchos de los tipos de archivo que Reproductor de Windows Media representan usan audio PCM.

Esta guía se divide en las secciones siguientes:



| Sección                                                                                | Descripción                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Información general del ejemplo de eco](echo-sample-overview.md)                                       | Describe los requisitos generales y las especificaciones del ejemplo. Describe cómo funciona el complemento.              |
| [Propiedades de ejemplo de eco](echo-sample-properties.md)                                   | Describe cómo modificar la propiedad de código del asistente y agregar métodos para la nueva propiedad necesaria para el ejemplo echo. |
| [Modificar la página de propiedades Echo Sample](modifying-the-echo-sample-property-page.md) | Muestra cómo modificar la implementación de la página de propiedades existente para que funcione con el ejemplo echo.                         |
| [Trabajar con recursos de streaming](working-with-streaming-resources.md)               | Muestra cómo agregar código para asignar y liberar un búfer necesario para el ejemplo de eco.                                |
| [Implementación de CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Describe cómo implementar el código que crea el efecto de eco.                                                   |
| [Uso del complemento DSP de ejemplo de eco](using-the-echo-sample-dsp-plug-in.md)             | Describe cómo usar el ejemplo completado.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación de complementos DE DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




