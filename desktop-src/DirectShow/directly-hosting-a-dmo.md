---
description: Hospedar directamente un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedar directamente un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806895"
---
# <a name="directly-hosting-a-dmo"></a>Hospedar directamente un DMO

En esta sección se describe cómo una aplicación puede actuar como cliente directo de DMO. La aplicación entrega la entrada a DMO, el DMO crea la salida y la aplicación utiliza la salida para la representación, el procesamiento posterior o cualquier otra cosa. La aplicación es responsable de los problemas, como la asignación de memoria, el control de tiempo y la sincronización, y el subprocesamiento. Estos requisitos dependerán de la naturaleza de la aplicación.

La información de esta sección también se aplica si está escribiendo un componente que actúa como una capa entre una aplicación y un DMO (por ejemplo, un control ActiveX que hospeda un DMO). Además, debe leer esta sección si está escribiendo un DMO, ya que describe la funcionalidad que debe implementar DMO.

Esta sección contiene los siguientes temas:

-   [Establecimiento de tipos de medios en DMO](setting-media-types-on-a-dmo.md)
-   [Procesamiento de datos en una DMO](processing-data-in-a-dmo.md)
-   [Procesamiento en contexto](in-place-processing.md)
-   [Flujos opcionales](optional-streams.md)
-   [Implementación de IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DMOs](using-dmos.md)
</dt> </dl>

 

 



