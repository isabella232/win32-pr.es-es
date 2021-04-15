---
description: Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe asignarle el nombre antes de que Monitor de red pueda mostrarlo en el Visor de eventos.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Asignar un nombre a una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669996"
---
# <a name="naming-an-event-reference-page"></a>Asignar un nombre a una página de referencia de eventos

Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe asignarle el nombre antes de que Monitor de red pueda mostrarlo en el Visor de eventos.

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

El identificador de evento también se encuentra en el miembro **EventIdent** de la estructura **NMEVENTDATA** .

</dd> </dl>

Para obtener más información acerca de la creación de un ERP, consulte los temas siguientes:

-   [Creación de páginas de referencia de eventos Expert y monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Escribir una página de referencia de eventos](writing-an-event-reference-page.md)
-   [Probar una página de referencia de eventos](testing-an-event-reference-page.md)

 

 



