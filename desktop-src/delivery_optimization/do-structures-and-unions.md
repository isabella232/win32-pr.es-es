---
title: Estructuras y uniones de DO
description: Las Optimización de distribución (DO) usan las estructuras siguientes.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 4bb78e2efa11dd067abf53a4fc7453aadb6c9a4844b4302701a466eec13806a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101758"
---
# <a name="do-structures-and-unions"></a>Estructuras y uniones de DO

Las Optimización de distribución (DO) [](do-interfaces.md) usan las estructuras siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La **BG_FILE_PROGRESS** proporciona información de progreso relacionada con el archivo, como el número de bytes transferidos. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La **BG_FILE_RANGE** estructura identifica un intervalo de bytes que se van a descargar de un archivo. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. Para los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | La **BITS_FILE_PROPERTY_VALUE** de datos proporciona el valor de propiedad del archivo DO basado en un valor de la [**enumeración BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) datos. |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | La **BITS_JOB_PROPERTY_VALUE** de datos proporciona el valor de propiedad del trabajo do en función del valor de la [**enumeración BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) datos. |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Usado por **IDOManager::EnumDownloads** para filtrar la enumeración de descargas por el valor de la propiedad específica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica un único intervalo de bytes que se van a descargar de un archivo. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica una matriz de intervalos de bytes que se van a descargar de un archivo. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Se usa para obtener el estado de una descarga específica. |
| [**DOSwarmStats**](doswarmstats.md) | Contiene campos para descargar y cargar estadísticas de un archivo. |