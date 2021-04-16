---
description: La creación de un filtro de captura que funcione con Monitor de red es un proceso de cinco pasos.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Creación de un filtro de captura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677735"
---
# <a name="creating-a-monitor-capture-filter"></a>Creación de un filtro de captura de monitor

La creación de un filtro de captura que funcione con Monitor de red es un proceso de cinco pasos:

-   [Establecer el valor de ETYPE o SAP Filter](writing-etypesap-filter-portion.md)
-   [Escribiendo filtro de ADDRESSTABLE](writing-addresstable-filter-portion.md)
-   [Escribir el filtro PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Recorte de un fotograma](clipping-a-frame.md)
-   [Implementar el código de filtro de captura](implementing-the-capture-filter-code.md)

Un [*filtro de captura*](c.md) es una serie de adiciones al BLOB NPP que selecciona qué fotogramas se pasan de vuelta al monitor. Si un monitor no modifica el BLOB NPP, el NPP pasará al modo promiscuo y enviará todo el tráfico de red al monitor. El NPP es más eficaz si puede reducir los datos entregados a un controlador, de modo que un monitor debe crear un filtro de captura. Un monitor establece su filtro de captura escribiendo en el BLOB NPP en la llamada a la función [Configure](imonitor-doconfigure.md) . A continuación, MCSVC llama a NPP con el BLOB NPP. Consulte [filtros de captura](capture-filters.md) para obtener más detalles sobre el filtro de captura, los [proveedores de paquetes de red](network-packet-providers.md) en NPPs y [monitor de red blobs](network-monitor-blobs.md) en las funciones de BLOB.

 

 



