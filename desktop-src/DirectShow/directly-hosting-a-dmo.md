---
description: Hospedaje directo de un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedaje directo de un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f421ed470ae1d39c04054e1cb4ec6252652ed2083ea336a58525f60a6e525b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982995"
---
# <a name="directly-hosting-a-dmo"></a>Hospedaje directo de un DMO

En esta sección se describe cómo una aplicación puede actuar como cliente directo de un DMO. La aplicación entrega la entrada al DMO, el DMO crea la salida y la aplicación usa la salida para la representación, el procesamiento adicional o cualquier otra cosa. La aplicación es responsable de problemas como la asignación de memoria, el tiempo y la sincronización, y el subproceso. Estos requisitos dependerán de la naturaleza de la aplicación.

La información de esta sección también se aplica si está escribiendo un componente que actúa como una capa entre una aplicación y un DMO (por ejemplo, un control ActiveX que hospeda un DMO). Además, debe leer esta sección si va a escribir un DMO, ya que describe la funcionalidad que el DMO debe implementar.

Esta sección contiene los siguientes temas:

-   [Establecer tipos de medios en un DMO](setting-media-types-on-a-dmo.md)
-   [Procesamiento de datos en un DMO](processing-data-in-a-dmo.md)
-   [Procesamiento en local](in-place-processing.md)
-   [Opcional Secuencias](optional-streams.md)
-   [Implementación de IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DDO](using-dmos.md)
</dt> </dl>

 

 



