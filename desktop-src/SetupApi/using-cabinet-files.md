---
description: Las funciones de configuración controlan internamente los gabinetes. Para enumerar y extraer archivos explícitamente de un archivador, puede llamar a la función SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Uso de archivos archivadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0479d9c6899de0899e24fd5b6c8aca59df1324b1402781a5630c8762822623b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964028"
---
# <a name="using-cabinet-files"></a>Uso de archivos archivadores

Las funciones de configuración controlan internamente los gabinetes. Para enumerar y extraer archivos explícitamente de un archivador, puede llamar a la [**función SetupIterateCabinet.**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)

En el tema siguiente se describe el procesamiento interno del gabinete de las funciones de instalación y cómo usar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). También se analizan las notificaciones enviadas por **SetupIterateCabinet** y el formato necesario de una rutina de devolución de llamada del gabinete para procesar esas notificaciones.

-   [Extracción de archivos de archivadores](extracting-files-from-cabinets.md)
-   [Crear una rutina de devolución de llamada de gabinete](creating-a-cabinet-callback-routine.md)

 

 



