---
description: Un filtro de captura es un elemento de una aplicación NPP que indica al controlador de Monitor de red (Nmnt.sys) qué tramas de datos de red se van a conservar y qué fotogramas se deben omitir.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Acerca de los filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667128"
---
# <a name="about-capture-filters"></a>Acerca de los filtros de captura

Un filtro de captura es un elemento de una aplicación NPP que indica al controlador de Monitor de red (Nmnt.sys) qué tramas de datos de red se van a conservar y qué fotogramas se deben omitir. La ventaja de configurar un filtro de captura es mayor eficiencia. No tiene que examinar los fotogramas capturados; el controlador de Monitor de red los examina. Este enfoque elimina la copia de fotogramas, lo que proporciona una ventaja de uso de memoria.

## <a name="capture-filter-structure"></a>Estructura del filtro de captura

Los filtros de captura se componen de tres elementos:

-   Configuración de ETYPE/SAP
-   Dirección
-   Coincidencia de patrones

Juntos, estos elementos evalúan lógicamente los fotogramas que se van a incluir o excluir durante la operación de una aplicación NPP. El filtro de captura proporciona coincidencias complejas y exclusiones de elementos Frame a la aplicación NPP.

Monitor de red implementa el filtro de captura a través de una estructura de datos, [**CAPTUREFILTER**](the-capturefilter-structure.md), pasada a NPP y, a continuación, se pasa al controlador de monitor de red cuando se inicia la captura.

Para obtener más información sobre las operaciones NPP y la funcionalidad BLOB, consulte [proveedores de paquetes de red](network-packet-providers.md) y [blobs monitor de red](network-monitor-blobs.md).

 

 



