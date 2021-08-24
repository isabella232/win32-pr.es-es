---
description: Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe nombrarlo para que Monitor de red pueda mostrarlo en el Visor de eventos.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Asignar un nombre a una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569991c5e5ac24e18476fe27727f4fad1c310c8fd4e9439062fdf91bfb344005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799695"
---
# <a name="naming-an-event-reference-page"></a>Asignar un nombre a una página de referencia de eventos

Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe nombrarlo para que Monitor de red pueda mostrarlo en el Visor de eventos.

Monitor de nombres y archivos ERP expertos con este formato:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**
</dt> <dd>

Nombre de archivo DLL, sin incluir la extensión de nombre de archivo.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Identificador de evento del ERP experto.

El identificador de evento también se encuentra en el **miembro EventIdent** de la estructura **NMEVENTDATA.**

</dd> </dl>

Para obtener más información sobre cómo crear un ERP, consulte los temas siguientes:

-   [Crear páginas de referencia de eventos expertos y de supervisión](creating-expert-and-monitor-event-reference-pages.md)
-   [Escribir una página de referencia de eventos](writing-an-event-reference-page.md)
-   [Probar una página de referencia de eventos](testing-an-event-reference-page.md)

 

 



