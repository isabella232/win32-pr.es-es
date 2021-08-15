---
description: Puede extraer archivos de un archivador de dos maneras. La primera y más sencilla es aprovechar el procesamiento automático del gabinete integrado en las funciones de configuración.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extracción de archivos de gabinetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887256"
---
# <a name="extracting-files-from-cabinets"></a>Extracción de archivos de gabinetes

Puede extraer archivos de un archivador de dos maneras. La primera y más sencilla es aprovechar el procesamiento automático del gabinete integrado en las funciones de configuración.

Las funciones de instalación, como [**SetupCommitFileQueue,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)y [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), comprueban la compresión en cada archivo. Si el archivo está en un archivador, las funciones buscan primero un archivo con ese nombre fuera del gabinete. Si se encuentra, las funciones instalan el archivo externo, omitiendo el archivo dentro del archivador. Esto le permite actualizar un único archivo dentro del gabinete sin volver a generar el gabinete.

Las funciones de instalación también realiza un seguimiento de los archivos de un archivador que se han recuperado, de modo que un archivo se extrae solo una vez, incluso si se instala varias veces.

La segunda manera de extraer archivos de un archivador es mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Esta función recorre en iteración cada archivo de un archivador y envía una notificación a una rutina de devolución de llamada para cada archivo encontrado. A continuación, la rutina de devolución de llamada devuelve un valor que indica si el archivo se debe extraer u omitir.

> [!Note]  
> La API de instalación no proporciona una rutina de devolución de llamada predeterminada para controlar las notificaciones de gabinete. Si llama explícitamente a [**SetupIterateCabinet,**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) debe proporcionar una rutina de devolución de llamada para procesar las notificaciones de gabinete que devuelve la función.

 

 

 



