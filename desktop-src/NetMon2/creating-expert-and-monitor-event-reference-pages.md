---
description: En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (O ERP e) y cómo implementarlas en un experto o en un monitor. Para obtener información sobre O ERP e y cómo usarlos con Monitor de red, consulte la página de referencia de eventos.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Creación de páginas de referencia de eventos Expert y monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652659"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Creación de páginas de referencia de eventos Expert y monitor

En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (O ERP e) y cómo implementarlas en un experto o en un monitor. Para obtener información sobre O ERP e y cómo usarlos con Monitor de red, consulte la [Página de referencia de eventos](event-reference-page.md).

Para desarrollar un nuevo ERP, el primer paso consiste en determinar los eventos que requieren O ERP e individuales para el [experto](experts.md) o el [monitor](monitors.md)personalizado. Debe crear O ERP e independientes para cada evento que desee mostrar en el Visor de eventos de Monitor de red. Por ejemplo, supongamos que:

-   Desarrolla un monitor denominado monitor de juegos y supervisor de existencias.
-   El monitor se encuentra en un archivo denominado Gamemon.dll.
-   El monitor genera dos eventos, juegos en ejecución y mis acciones de Internet.
-   Planea desarrollar dos O ERP e, Gamemon1.htm y Gamemon2.htm.

> [!Note]  
> No es necesario tener una correspondencia uno a uno de O ERP e para supervisar o realizar eventos expertos.

 

Una vez que haya establecido una lista de O ERP e únicos, siga estos pasos para crear cada ERP.

-   [Escriba el documento de origen HTML](writing-an-event-reference-page.md).
-   Guarde el archivo de código fuente HTML [y asígnele un nombre](naming-an-event-reference-page.md) como archivo. htm.
-   [Pruebe el ERP](testing-an-event-reference-page.md) con el experto o el monitor completado.

 

 



