---
description: La API de distribución del mismo nivel define los siguientes tipos de datos.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de datos de la API de distribución del mismo nivel (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667412"
---
# <a name="peer-distribution-api-data-types"></a>Tipos de datos de la API de distribución del mismo nivel

La API de distribución del mismo nivel define los siguientes tipos de datos.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Tipo de datos                                                                                                                     | Descripción                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_identificador de instancia de PEERDIST \_**          | Identificador asociado a la instancia de distribución del mismo nivel. [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)crea este identificador y se usa en la mayoría de las operaciones de distribución del mismo nivel.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_identificador de contenido de PEERDIST \_**             | Identificador asociado con el contenido. Este identificador se crea mediante [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) y se hace referencia a él al abrir, cerrar, agregar o publicar contenido.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_identificador de CONTENTINFO de PEERDIST \_** | Identificador asociado a la información de contenido. [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)crea este identificador y se utiliza al recuperar la información de contenido codificado.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_identificador de flujo de PEERDIST \_**                | Identificador asociado a un flujo de datos. Este identificador se crea mediante [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) y se hace referencia a él al publicar, cerrar o agregar a contenido transmitido.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 Professional \[\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Peerdist. h</dt> </dl> |



 

 




