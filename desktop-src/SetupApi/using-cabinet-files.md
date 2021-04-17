---
description: Las funciones de configuración controlan internamente los contenedores. Para enumerar y extraer explícitamente los archivos de un archivo. cab, puede llamar a la función SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Uso de archivos. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668289"
---
# <a name="using-cabinet-files"></a>Uso de archivos. cab

Las funciones de configuración controlan internamente los contenedores. Para enumerar y extraer explícitamente los archivos de un archivo. cab, puede llamar a la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

En el siguiente tema se describe el procesamiento del archivo. cab interno de las funciones de instalación y cómo usar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). También se describen las notificaciones enviadas por **SetupIterateCabinet** y el formato requerido de una rutina de devolución de llamada de archivador para procesar esas notificaciones.

-   [Extraer archivos de los archivadores](extracting-files-from-cabinets.md)
-   [Crear una rutina de devolución de llamada de archivador](creating-a-cabinet-callback-routine.md)

 

 



