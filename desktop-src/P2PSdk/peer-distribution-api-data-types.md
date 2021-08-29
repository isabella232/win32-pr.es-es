---
description: La API de distribución del mismo nivel define los siguientes tipos de datos.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de datos de la API de distribución del mismo nivel (Peerdist.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ecfb7a9a90cb5ef2d79a20356ea8ea39f708874e85c3119dd4407a0a3758146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776085"
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
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**IDENTIFICADOR DE INSTANCIA \_ PEERDIST \_**          | Identificador asociado a la instancia de distribución del mismo nivel. [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)crea este identificador y se usa en la mayoría de las operaciones de distribución del mismo nivel.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**IDENTIFICADOR DE CONTENIDO \_ \_ PEERDIST**             | Identificador asociado al contenido. [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) crea este identificador y se hace referencia a él al abrir, cerrar, agregar o publicar contenido.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**IDENTIFICADOR \_ CONTENTINFO DE PEERDIST \_** | Identificador asociado a la información de contenido. [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)crea este identificador y se usa al recuperar información de contenido codificada.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**IDENTIFICADOR DE FLUJO PEERDIST \_ \_**                | Identificador asociado a un flujo de datos. [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) crea este identificador y se hace referencia a él al publicar, cerrar o agregar contenido transmitido.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones Professional \[ escritorio\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Header<br/>                   | <dl> <dt>Peerdist.h</dt> </dl> |



 

 




