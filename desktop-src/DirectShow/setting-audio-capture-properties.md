---
description: Establecer propiedades de captura de audio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Establecer propiedades de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31afe61d4641906391934bafe4c3acb8a911a9fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274609"
---
# <a name="setting-audio-capture-properties"></a>Establecer propiedades de captura de audio

Cada pin de entrada del filtro de captura de audio expone la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) . Use esta interfaz para habilitar o deshabilitar una entrada determinada, llamando al método [**IAMAudioInputMixer::p UT \_ enable**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) en el PIN. También puede usar esta interfaz para establecer las propiedades de una entrada, como los niveles de bajos, agudos y volúmenes. Si va a capturar varias entradas a la vez, puede controlar los niveles de graves, agudos y volúmenes generales a través de la interfaz **IAMAudioInputMixer** en el propio filtro.

La velocidad de muestreo y los formatos de audio disponibles para la captura vienen determinados por el controlador. Use la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en el PIN de salida del filtro de captura de audio para enumerar los formatos y las velocidades de muestreo disponibles y establecer el formato deseado. El filtro puede conectarse de nivel inferior a cualquier filtro que acepte el tipo de medio del terminal de salida.

El filtro de captura de audio también expone la interfaz [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) . Esta interfaz es útil para controlar la cantidad de latencia en la vista previa de audio. De forma predeterminada, el filtro de captura de audio utiliza un tamaño de búfer de medio segundo. Este tamaño de búfer es óptimo para la captura, pero produce un retraso de la vista previa de medio segundo. Para reducir la latencia, llame al método [**IAMBufferNegotiation:: SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) antes de conectar el PIN de salida del filtro de captura de audio. Este método toma un puntero a la estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) . Use el miembro **cbBuffer** para especificar el tamaño del búfer, en bytes. Un búfer de 80 milisegundos suele ser seguro, pero los búferes de 30 o 40 milisegundos pueden ser suficientes. Si los búferes son demasiado pequeños, la calidad del sonido se degradará.

 

 



