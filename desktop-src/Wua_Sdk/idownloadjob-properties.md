---
description: La interfaz IDownloadJob define las siguientes propiedades.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propiedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cdd4f95a14df215017f9fd628497d15c6c7410e4a82cbfb53c076b2112899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049350"
---
# <a name="idownloadjob-properties"></a>Propiedades de IDownloadJob

La [**interfaz IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define las siguientes propiedades.



| Propiedad                                        | Descripción                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Obtiene el objeto de estado específico del autor de la llamada que se pasa al [**método IUpdateDownloader.BeginDownload.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload)           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Obtiene la configuración que indica si la llamada a [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) se procesó completamente. |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones especificadas en una descarga.                                                  |



 

 

 



