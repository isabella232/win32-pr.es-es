---
title: Estructuras y uniones
description: Las interfaces de optimización de entrega (DO) usan las siguientes estructuras.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 860672e72e1e5f134382fd46cd9b36d1d411361e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149462"
---
# <a name="do-structures-and-unions"></a>Estructuras y uniones

Las [interfaces](do-interfaces.md) de optimización de entrega (do) usan las siguientes estructuras.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | La estructura **BG_FILE_PROGRESS** proporciona información de progreso relacionada con archivos, como el número de bytes transferidos. |
| [**BG_FILE_RANGE**](bg-file-range.md) | La estructura **BG_FILE_RANGE** identifica un intervalo de bytes que se van a descargar de un archivo. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | La estructura **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. En el caso de los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | La estructura **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | La Unión **BITS_FILE_PROPERTY_VALUE** proporciona el valor de propiedad del archivo do basado en un valor de la enumeración [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) . |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | La Unión **BITS_JOB_PROPERTY_VALUE** proporciona el valor de propiedad del trabajo do basándose en el valor de la enumeración [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) . |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Lo usa **IDOManager:: EnumDownloads** para filtrar la enumeración downloads por el valor de la propiedad específica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica un intervalo único de bytes que se va a descargar de un archivo. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica una matriz de intervalos de bytes que se van a descargar de un archivo. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Se usa para obtener el estado de una descarga específica. |
| [**DOSwarmStats**](doswarmstats.md) | Contiene campos para las estadísticas de descarga y carga de un archivo. |