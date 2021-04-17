---
description: Puede extraer archivos de un archivo. cab de dos maneras. La primera y la manera más sencilla es aprovechar el procesamiento automático de los contenedores integrados en las funciones de configuración.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraer archivos de los archivadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666646"
---
# <a name="extracting-files-from-cabinets"></a>Extraer archivos de los archivadores

Puede extraer archivos de un archivo. cab de dos maneras. La primera y la manera más sencilla es aprovechar el procesamiento automático de los contenedores integrados en las funciones de configuración.

Las funciones de instalación, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)y [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), comprueban la compresión en cada archivo. Si el archivo está en un archivo. cab, las funciones buscan primero un archivo con ese nombre fuera del archivo. cab. Si se encuentra, las funciones instalan el archivo externo, omitiendo el archivo dentro del archivo. cab. Esto le permite actualizar un solo archivo dentro del archivo. cab sin volver a generarlo.

Las funciones de configuración también realizan un seguimiento de los archivos de un archivo. cab que se han recuperado, de modo que un archivo se extrae solo una vez, incluso si se instala varias veces.

La segunda manera de extraer archivos de un archivo. cab es mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Esta función recorre en iteración todos los archivos de un archivo. cab y envía una notificación a una rutina de devolución de llamada para cada archivo encontrado. A continuación, la rutina de devolución de llamada devuelve un valor que indica si el archivo debe extraerse u omitirse.

> [!Note]  
> La API de instalación no proporciona una rutina de devolución de llamada predeterminada para controlar las notificaciones del archivo. Si llama explícitamente a [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , debe proporcionar una rutina de devolución de llamada para procesar las notificaciones del archivo CAB que devuelve la función.

 

 

 



