---
description: Un filtro de captura es un elemento de una aplicación de NPP que indica al controlador Monitor de red (Nmnt.sys) qué fotogramas de datos de red se conservarán y qué fotogramas se omitirán.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Acerca de los filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0d1eee25915c30b8ddffc475545cbd7f7d04d0fdcecf4119480b737980cd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911365"
---
# <a name="about-capture-filters"></a>Acerca de los filtros de captura

Un filtro de captura es un elemento de una aplicación de NPP que indica al controlador Monitor de red (Nmnt.sys) qué fotogramas de datos de red se conservarán y qué fotogramas se omitirán. La ventaja de establecer un filtro de captura es una mayor eficacia. No es necesario examinar los fotogramas capturados; el Monitor de red los examina. Este enfoque elimina la copia de fotogramas, lo que proporciona una ventaja de uso de memoria.

## <a name="capture-filter-structure"></a>Estructura de filtro de captura

Los filtros de captura constan de tres elementos:

-   Configuración de Etype/SAP
-   Dirección
-   Coincidencia de patrones

Juntos, estos elementos evalúan lógicamente qué fotogramas incluir o excluir durante el funcionamiento de una aplicación NPP. El filtro de captura proporciona coincidencias complejas y exclusiones de elementos de marco a la aplicación NPP.

Monitor de red implementa el filtro de captura a través de una estructura de datos, [**CAPTUREFILTER,**](the-capturefilter-structure.md)que se pasa al NPP y, a continuación, se pasa al controlador Monitor de red cuando se inicia la captura.

Para obtener más información sobre las operaciones de NPP y la funcionalidad blob, vea [Proveedores de paquetes de](network-packet-providers.md) red y Monitor de red [BLOBS.](network-monitor-blobs.md)

 

 



