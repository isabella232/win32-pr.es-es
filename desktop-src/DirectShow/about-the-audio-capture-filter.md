---
description: Acerca del filtro de captura de audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Acerca del filtro de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152589"
---
# <a name="about-the-audio-capture-filter"></a>Acerca del filtro de captura de audio

DirectShow habilita la captura de las entradas analógicas en una tarjeta de sonido a través del [filtro de captura de audio](audio-capture-filter.md). Este filtro usa las API de Wave *XXX* para controlar cualquier dispositivo cuyo controlador admita estas API. Cada tarjeta del sistema se representa mediante una instancia independiente del filtro.

El filtro de captura de audio expone cada entrada de la tarjeta, como el micrófono o la entrada MIDI, como un PIN de entrada. Los pin de entrada representan lo que el controlador expone como líneas de origen de audio. Sin embargo, los datos no viajan a través de estos PIN de entrada y no se conectan a otros filtros de DirectShow. Simplemente proporcionan una manera para que una aplicación controle las entradas. La aplicación puede usar un PIN de entrada para habilitar o deshabilitar la entrada, o para establecer propiedades de mezcla como la ecualización de graves, la ecualización de agudos, la panorámica, etc. La cantidad de control que está disponible depende del controlador. Para comprender completamente y aprovechar las capacidades de una tarjeta de sonido determinada, necesitará la documentación del fabricante de la tarjeta.

> [!Note]  
> Puede capturar desde el CD-Audio entrada, pero esta secuencia de audio ya ha pasado por el convertidor digital a analógico, por lo que se producirá una pérdida de calidad de sonido del CD original.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



