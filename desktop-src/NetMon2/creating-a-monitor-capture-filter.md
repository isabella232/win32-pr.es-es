---
description: La creación de un filtro de captura que funciona Monitor de red es un proceso de cinco pasos.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Crear un filtro de captura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9e58aebd18f861ad8fc36c4d6f718ff3e3694c828b23436764e288d083fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064164"
---
# <a name="creating-a-monitor-capture-filter"></a>Crear un filtro de captura de monitor

La creación de un filtro de captura que funciona Monitor de red es un proceso de cinco pasos:

-   [Establecimiento del tipo Etype o el filtro de SAP](writing-etypesap-filter-portion.md)
-   [Escribir filtro ADDRESSTABLE](writing-addresstable-filter-portion.md)
-   [Escribir el filtro PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Recorte de un marco](clipping-a-frame.md)
-   [Implementación del código de filtro de captura](implementing-the-capture-filter-code.md)

Un [*filtro de*](c.md) captura es una serie de adiciones al BLOB de NPP que selecciona qué fotogramas se pasan de nuevo al monitor. Si un monitor no modifica el BLOB de NPP, el NPP pasará al modo promiscuo y enviará todo el tráfico de red al monitor. El NPP es más eficaz si puede reducir los datos entregados a un controlador, por lo que un monitor debe crear un filtro de captura. Un monitor establece su filtro de captura escribiendo en el BLOB de NPP en la llamada a la [función DoConfigure.](imonitor-doconfigure.md) A continuación, MCSVC llama al NPP con el BLOB de NPP. Consulte [Filtros de captura](capture-filters.md) para obtener más información sobre el filtro de captura, proveedores de paquetes de red en NPP y Monitor de red [blobs en](network-monitor-blobs.md) funciones BLOB. [](network-packet-providers.md)

 

 



