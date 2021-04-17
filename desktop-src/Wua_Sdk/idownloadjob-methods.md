---
description: La interfaz IDownloadJob define los siguientes métodos.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Métodos IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542294"
---
# <a name="idownloadjob-methods"></a>Métodos IDownloadJob

La interfaz [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define los siguientes métodos.



| Método                                            | Descripción                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Reparación**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Espera a que se complete una operación asincrónica y libera todas las devoluciones de llamada.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Devuelve una interfaz [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) que describe el progreso actual de una descarga. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Realiza una solicitud para finalizar una descarga asincrónica.                                                                       |



 

 

 



