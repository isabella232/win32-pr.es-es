---
description: Hospedaje directo de un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedaje directo de un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061225"
---
# <a name="directly-hosting-a-dmo"></a>Hospedaje directo de un DMO

En esta sección se describe cómo una aplicación puede actuar como el cliente directo de un DMO. La aplicación entrega la entrada al DMO, el DMO crea la salida y la aplicación usa la salida para la representación, el procesamiento adicional o cualquier otra cosa. La aplicación es responsable de problemas como la asignación de memoria, el control de tiempo y la sincronización, y el subprocesamiento. Estos requisitos dependerán de la naturaleza de la aplicación.

La información de esta sección también se aplica si está escribiendo un componente que actúa como una capa entre una aplicación y un DMO (por ejemplo, un control ActiveX que hospeda un DMO). Además, debe leer esta sección si va a escribir un DMO, ya que describe la funcionalidad que el DMO debe implementar.

Esta sección contiene los siguientes temas:

-   [Establecer tipos de medios en un DMO](setting-media-types-on-a-dmo.md)
-   [Procesamiento de datos en un DMO](processing-data-in-a-dmo.md)
-   [Procesamiento in-place](in-place-processing.md)
-   [Opcional Secuencias](optional-streams.md)
-   [Implementación de IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DDO](using-dmos.md)
</dt> </dl>

 

 



