---
title: El ejemplo echo
description: El ejemplo echo
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Complementos de Media Player de Windows, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- Complementos de procesamiento de señal digital, información general de ejemplo de eco
- Complementos DSP, información general de ejemplo de eco
- Guía de programación, Complementos DSP
- ejemplos, Complementos DSP
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f2dfe6a59257b8a16dc31a5b4cb751d649cd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994317"
---
# <a name="the-echo-sample"></a>El ejemplo echo

El Asistente para complementos de Windows Media Player puede crear un proyecto de complemento de DSP para Microsoft Visual C++. El código predeterminado generado por el asistente permite al usuario proporcionar un factor de escala entre 0 y 1, que es utilizado por el programa como multiplicador para los ejemplos de audio. Se trata de una implementación muy sencilla que puede estudiar para comprender cómo Windows Media Player interactúa con los complementos de DSP. La información de la sección denominada [acerca de los complementos DSP](about-dsp-plug-ins.md) puede ayudarle a entender la implementación predeterminada.

El ejemplo que se describe en esta sección es un poco más complejo. Este ejemplo permite al usuario especificar un tiempo de retardo, en milisegundos, y un nivel de efecto. El código usa estos valores para generar un efecto de eco al reproducir archivos que contienen audio de modulación por pulsos (PCM). Muchos de los tipos de archivo que Windows Media Player representa usan PCM audio.

Esta guía se divide en las siguientes secciones:



| Sección                                                                                | Descripción                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Información general del ejemplo echo](echo-sample-overview.md)                                       | Describe los requisitos generales y las especificaciones para el ejemplo. Describe cómo funciona el complemento.              |
| [Eco de propiedades de ejemplo](echo-sample-properties.md)                                   | Describe cómo modificar la propiedad del código del asistente y agregar métodos para la nueva propiedad requerida para el ejemplo echo. |
| [Modificar la página de propiedades de ejemplo echo](modifying-the-echo-sample-property-page.md) | Muestra cómo modificar la implementación de la página de propiedades existente para que funcione con el ejemplo echo.                         |
| [Trabajar con recursos de streaming](working-with-streaming-resources.md)               | Muestra cómo agregar código para asignar y liberar un búfer necesario para el ejemplo echo.                                |
| [Implementación de CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Describe cómo implementar el código que crea el efecto de eco.                                                   |
| [Usar el complemento DSP de ejemplo echo](using-the-echo-sample-dsp-plug-in.md)             | Describe cómo utilizar el ejemplo completado.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación de complementos DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




