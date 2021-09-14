---
description: La API de distribución del mismo nivel define los siguientes tipos de datos.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de datos de la API de distribución del mismo nivel (Peerdist.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069221"
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
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**IDENTIFICADOR DE CONTENIDO \_ DE PEERDIST \_**             | Identificador asociado al contenido. [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) crea este identificador y se hace referencia a él al abrir, cerrar, agregar o publicar contenido.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**IDENTIFICADOR \_ CONTENTINFO DE PEERDIST \_** | Identificador asociado a la información de contenido. [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)crea este identificador y se usa al recuperar información de contenido codificada.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**IDENTIFICADOR DE FLUJO \_ PEERDIST \_**                | Identificador asociado a un flujo de datos. [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) crea este identificador y se hace referencia a él al publicar, cerrar o agregar contenido transmitido.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones Professional \[ escritorio\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Peerdist.h</dt> </dl> |



 

 




