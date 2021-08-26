---
description: Establecer propiedades de captura de audio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Establecer propiedades de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078815"
---
# <a name="setting-audio-capture-properties"></a>Establecer propiedades de captura de audio

Cada pin de entrada en el filtro de captura de audio expone la [**interfaz IAMAudioInputMixer.**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) Use esta interfaz para habilitar o deshabilitar una entrada determinada, llamando al método [**IAMAudioInputMixer::p ut \_ Enable**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) en el pin. Use también esta interfaz para establecer las propiedades de una entrada, como los niveles de bajo, triple y volumen. Si va a capturar varias entradas a la vez, puede controlar los niveles generales de bajo, triple y volumen a través de la interfaz **IAMAudioInputMixer** en el propio filtro.

El controlador determina las velocidades de muestreo y los formatos de audio disponibles para la captura. Use la [**interfaz IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en el pin de salida del filtro de captura de audio para enumerar las velocidades de muestreo y los formatos disponibles y establecer el formato deseado. El filtro puede conectarse de bajada a cualquier filtro que acepte el tipo de medio del pin de salida.

El filtro de captura de audio también expone la [**interfaz IAMBufferNegotiation.**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) Esta interfaz es útil para controlar la cantidad de latencia en la versión preliminar de audio. De forma predeterminada, el filtro Captura de audio usa un tamaño de búfer de medio segundo. Este tamaño de búfer es óptimo para la captura, pero provoca un retraso en la versión preliminar de medio segundo. Para reducir la latencia, llame al método [**IAMBufferNegotiation::SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) antes de conectar el pin de salida del filtro de captura de audio. Este método toma un puntero a la [**estructura ALLOCATOR \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Use el **miembro cbBuffer** para especificar el tamaño del búfer, en bytes. Un búfer de 80 milisegundos suele ser seguro, pero los búferes de 30 o 40 milisegundos pueden ser suficientes. Si los búferes son demasiado pequeños, la calidad del sonido se degradará.

 

 



