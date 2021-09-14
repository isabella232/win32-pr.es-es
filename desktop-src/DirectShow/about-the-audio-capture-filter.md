---
description: Acerca del filtro de captura de audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Acerca del filtro de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162458"
---
# <a name="about-the-audio-capture-filter"></a>Acerca del filtro de captura de audio

DirectShow permite la captura de las entradas análogas en una tarjeta de sonido a través del [filtro de captura de audio](audio-capture-filter.md). Este filtro usa las API waveIn *XXX* para controlar cualquier dispositivo cuyo controlador admita estas API. Cada tarjeta del sistema se representa mediante una instancia independiente del filtro.

El filtro De captura de audio expone cada entrada de la tarjeta, como el micrófono o la entrada MIDI, como un pin de entrada. Los pines de entrada representan lo que el controlador expone como líneas de origen de audio. Sin embargo, ningún dato viaja a través de estos pines de entrada y no se conectan a otros filtros DirectShow datos. Simplemente proporcionan una manera de que una aplicación controle las entradas. La aplicación puede usar un pin de entrada para habilitar o deshabilitar la entrada, o para establecer propiedades de combinación, como la igualdad de asas, la igualdad triple, la panorámica, etc. La cantidad de control disponible depende del controlador. Para comprender y aprovechar completamente las funcionalidades de una tarjeta de sonido determinada, necesitará la documentación del fabricante de la tarjeta.

> [!Note]  
> Puede capturar desde la entrada CD-Audio, pero esta secuencia de audio ya ha pasado por el convertidor de digital a análogo, por lo que habrá una pérdida de calidad de sonido del CD original.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



