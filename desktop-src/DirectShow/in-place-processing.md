---
description: In-Place procesamiento
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677161"
---
# <a name="in-place-processing"></a>In-Place procesamiento

Ciertas transformaciones de datos se pueden realizar mediante la modificación directa de los datos. Esto se denomina procesamiento *en contexto* . Muchos efectos de audio y vídeo se pueden realizar de esta manera. Si un DMO admite el procesamiento en contexto, expone la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) . El procesamiento en contexto suele ser más eficaz que el uso de búferes independientes para la salida. (Una excepción principal es cuando el búfer reside en la memoria de vídeo. En esta situación, las operaciones de lectura son mucho más lentas que las operaciones de escritura, por lo que no se recomienda el procesamiento en contexto).

Para procesar los datos en su lugar, el cliente realiza una llamada única al método [**IMediaObjectInPlace::P rador**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , en lugar de llamadas independientes a **ProcessInput** y **ProcessOutput**. El método **Process** es sincrónico; todo el procesamiento se produce dentro de la llamada. Además, el procesamiento en contexto no usa objetos **IMediaBuffer** . El método **Process** toma un puntero directamente al búfer de memoria.

Un DMO que admite el procesamiento en contexto todavía debe implementar la interfaz **IMediaObject** , incluidos los métodos **ProcessInput** y **ProcessOutput** . El cliente puede elegir si desea usar el procesamiento en contexto o utilizar búferes independientes. Sin embargo, no mezcle los dos tipos de procesamiento. Si llama al **proceso**, no llame a **ProcessInput** o **ProcessOutput** y viceversa.

**Colas de efectos**

Una DMO en contexto podría crear una salida adicional después de que la entrada se detenga. Esto se denomina *cola de efectos*. Por ejemplo, un efecto de reverberación continúa después de que la entrada alcance el silencio. Si hay una cola de efectos, el método **Process** devuelve S \_ false. Una vez que la aplicación ha procesado todos sus datos, puede generar la cola del efecto mediante el envío de búferes vacíos al método de **proceso** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedar directamente un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



