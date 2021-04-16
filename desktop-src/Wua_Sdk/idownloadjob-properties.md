---
description: La interfaz IDownloadJob define las siguientes propiedades.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propiedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705741"
---
# <a name="idownloadjob-properties"></a>Propiedades de IDownloadJob

La interfaz [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define las siguientes propiedades.



| Propiedad                                        | Descripción                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Obtiene el objeto de estado específico del llamador que se pasa al método [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Obtiene el valor que indica si la llamada a [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) se procesó completamente. |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican en una descarga.                                                  |



 

 

 



