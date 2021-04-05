---
description: La interfaz IDownloadProgress define las siguientes propiedades.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propiedades de IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001202"
---
# <a name="idownloadprogress-properties"></a>Propiedades de IDownloadProgress

La interfaz [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) define las siguientes propiedades.



| Propiedad                                                                               | Descripción                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Obtiene una cadena que especifica la cantidad de datos transferidos para el archivo de contenido o los archivos de la actualización que se está descargando, en bytes.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Obtiene una cadena que calcula la cantidad de datos que se deben transferir para el archivo de contenido o los archivos de la actualización que se está descargando, en bytes. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Obtiene un valor de enumeración [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) que especifica la fase de la descarga que está actualmente en curso.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Obtiene un valor de índice de base cero que especifica la actualización que se está descargando actualmente cuando se han seleccionado varias actualizaciones.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Obtiene una estimación del porcentaje de la actualización actual que se ha descargado.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Obtiene una estimación del porcentaje de todas las actualizaciones que se han descargado.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Obtiene una cadena que especifica la cantidad total de datos que se han descargado, en bytes.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Obtiene una cadena que representa la estimación de la cantidad total de datos que se van a descargar, en bytes.                                        |



 

 

 



