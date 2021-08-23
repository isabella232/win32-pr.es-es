---
description: En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (ERP) y cómo implementarlas en un experto o monitor. Para obtener información sobre los ERP y cómo usarlos con Monitor de red, vea Página de referencia de eventos.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Crear páginas de referencia de eventos expertos y de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5826ab0aaa71461f6b4e56b9330e00c5af6aae26952d84af88c380da6dfe41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144238"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Crear páginas de referencia de eventos expertos y de supervisión

En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (ERP) y cómo implementarlas en un experto o monitor. Para obtener información sobre los ERP y cómo usarlos con Monitor de red, vea [Página de referencia de eventos](event-reference-page.md).

Para desarrollar un nuevo ERP, el primer paso consiste en [](experts.md) determinar los eventos que requieren ERP individuales para el experto o [monitor personalizado.](monitors.md) Debe crear ERP independientes para cada evento que desee mostrar en el Monitor de red Visor de eventos. Por ejemplo, supongamos que:

-   Desarrollará un monitor denominado Game Monitor y Stock Watcher.
-   El monitor se encuentra en un archivo denominado Gamemon.dll.
-   El monitor genera dos eventos, Game Running y My Internet Stock Soars.
-   Tiene previsto desarrollar dos ERP, Gamemon1.htm y Gamemon2.htm.

> [!Note]  
> No es necesario tener una correspondencia uno a uno de los ERP para supervisar o eventos expertos.

 

Después de haber establecido una lista de ERP únicos, siga estos pasos para crear cada ERP.

-   [Escriba el documento de origen HTML](writing-an-event-reference-page.md).
-   [Guarde y asigne un](naming-an-event-reference-page.md) nombre al archivo de código fuente HTML .htm archivo.
-   [Pruebe erp con](testing-an-event-reference-page.md) el experto o monitor completado.

 

 



