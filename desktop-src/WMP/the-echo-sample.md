---
title: Ejemplo de eco
description: Ejemplo de eco
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Reproductor de Windows Media complementos, Información general del ejemplo de eco
- complementos, información general de ejemplo de eco
- complementos de procesamiento de señales digitales, información general de ejemplo de eco
- Complementos DE DSP, Información general del ejemplo de eco
- guía de programación, complementos DE DSP
- samples,DSP plug-ins
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762795"
---
# <a name="the-echo-sample"></a>Ejemplo de eco

El Reproductor de Windows Media complemento de Microsoft Visual C++ puede crear un proyecto de complemento DE DSP para Microsoft Visual C++. El código predeterminado generado por el asistente permite al usuario proporcionar un factor de escala entre 0 y 1, que el programa usa como multiplicador para las muestras de audio. Se trata de una implementación muy sencilla que puede estudiar para comprender Reproductor de Windows Media interactúa con los complementos de DSP. La información de la sección denominada [About DSP Plug-ins](about-dsp-plug-ins.md) (Acerca de los complementos de DSP) puede ayudarle a comprender la implementación predeterminada.

El ejemplo descrito en esta sección es un poco más complejo. Este ejemplo permite al usuario especificar un tiempo de retraso, en milisegundos, y un nivel de efecto. El código usa estos valores para generar un efecto de eco al reproducir archivos que contienen audio de pulsación de codificación (PCM). Muchos de los tipos de archivo que Reproductor de Windows Media utilizan audio PCM.

Esta guía se divide en las secciones siguientes:



| Sección                                                                                | Descripción                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Información general del ejemplo de eco](echo-sample-overview.md)                                       | Describe los requisitos generales y las especificaciones del ejemplo. Describe cómo funciona el complemento.              |
| [Propiedades de ejemplo de eco](echo-sample-properties.md)                                   | Describe cómo modificar la propiedad de código del asistente y agregar métodos para la nueva propiedad necesaria para el ejemplo de eco. |
| [Modificar la página de propiedades Echo Sample](modifying-the-echo-sample-property-page.md) | Muestra cómo modificar la implementación de la página de propiedades existente para que funcione con el ejemplo de eco.                         |
| [Trabajar con recursos de streaming](working-with-streaming-resources.md)               | Muestra cómo agregar código para asignar y liberar un búfer necesario para el ejemplo de eco.                                |
| [Implementación de CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Describe cómo implementar el código que crea el efecto de eco.                                                   |
| [Uso del complemento DSP de ejemplo de eco](using-the-echo-sample-dsp-plug-in.md)             | Describe cómo usar el ejemplo completado.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación de complementos DE DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




