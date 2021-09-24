---
title: Optimización de distribución estructuras y uniones
description: Las Optimización de distribución usan las estructuras siguientes.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 035b465d61cfcee78a20fda0d275e1eece1a78c5
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520485"
---
# <a name="delivery-optimization-structures-and-unions"></a>Optimización de distribución estructuras y uniones

Las Optimización de distribución [usan](do-interfaces.md) las estructuras siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La **BG_FILE_PROGRESS** proporciona información de progreso relacionada con el archivo, como el número de bytes transferidos. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La **BG_FILE_RANGE** estructura identifica un intervalo de bytes que se van a descargar de un archivo. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. Para los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | La **BITS_FILE_PROPERTY_VALUE** de datos proporciona el valor de propiedad del archivo Optimización de distribución basado en un valor de la [**enumeración BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) datos. |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | La **BITS_JOB_PROPERTY_VALUE** de datos proporciona el valor de propiedad del Optimización de distribución trabajo basado en el valor de la [**enumeración BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) datos. |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Lo usa **IDOManager::EnumDownloads** para filtrar la enumeración de descargas por el valor de la propiedad específica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica un único intervalo de bytes que se van a descargar de un archivo. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica una matriz de intervalos de bytes que se van a descargar de un archivo. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Se usa para obtener el estado de una descarga específica. |
| [**DOSwarmStats**](doswarmstats.md) | Contiene campos para descargar y cargar estadísticas de un archivo. |