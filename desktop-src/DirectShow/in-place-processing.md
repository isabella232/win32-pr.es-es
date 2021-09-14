---
description: In-Place procesamiento
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063251"
---
# <a name="in-place-processing"></a>In-Place procesamiento

Determinadas transformaciones de datos se pueden realizar modificando directamente los datos. Esto se denomina *procesamiento* local. Muchos efectos de audio y vídeo se pueden realizar de esta manera. Si un DMO admite el procesamiento local, expone la [**interfaz IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) El procesamiento local suele ser más eficaz que usar búferes independientes para la salida. (Una excepción principal es cuando el búfer reside en la memoria de vídeo. En esa situación, las operaciones de lectura son mucho más lentas que las operaciones de escritura, por lo que no se recomienda el procesamiento local).

Para procesar los datos en su lugar, el cliente realiza una única llamada al método [**IMediaObjectInPlace::P rocess,**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) en lugar de realizar llamadas independientes a **ProcessInput** y **ProcessOutput**. El **método Process** es sincrónico; todo el procesamiento se produce dentro de la llamada. Además, el procesamiento local no usa objetos **IMediaBuffer.** El **método Process** toma un puntero directamente al búfer de memoria.

Un DMO que admite el procesamiento local todavía debe implementar la interfaz **IMediaObject,** incluidos los métodos **ProcessInput** **y ProcessOutput.** El cliente puede elegir si desea usar el procesamiento local o usar búferes independientes. Sin embargo, no mezcle los dos tipos de procesamiento. Si llama a **Process**, no llame a **ProcessInput** o **ProcessOutput** y viceversa.

**Colas de efecto**

Una configuración en DMO podría crear alguna salida adicional después de que se detenga la entrada. Esto se denomina cola *de efecto*. Por ejemplo, un efecto de reverberación continúa después de que la entrada alcance el silencio. Si hay un final de efecto, el **método Process** devuelve S \_ FALSE. Una vez que la aplicación ha procesado todos sus datos, puede generar el final del efecto mediante el envío de búferes vacíos al **método Process.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedaje directo de un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



