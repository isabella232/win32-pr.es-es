---
title: Puntos de conexión
description: Un objeto de punto de conexión contiene datos sobre una o varias instancias de un servicio disponible en la red.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- puntos de conexión de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0b7a4c8ddbf592bba0ed39e2eb8f93faf863e6ebff7081865466b6522c98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022055"
---
# <a name="connection-points"></a>Puntos de conexión

Un objeto de punto de conexión contiene datos sobre una o varias instancias de un servicio disponible en la red. La [**clase de objeto connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) es la clase base abstracta de la que se derivan los objetos que representan los recursos conectables Active Directory Domain Services se derivan. En la ilustración siguiente se muestran algunas de las clases de objeto derivadas de la **clase de objeto connectionPoint.**

![Clases de objeto derivadas de la clase de objeto connectionpoint](images/connection-points.png)

En la tabla siguiente se enumeran las subclases inmediatas de la [**clase connectionPoint.**](/windows/desktop/ADSchema/c-connectionpoint)



| Clase de objeto                                                    | Descripción                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Objetos de punto de conexión de servicio (SCP) para publicar datos que las aplicaciones cliente usan para enlazar a un servicio. Para obtener más información, [vea Publicación con puntos de conexión de servicio (SCP).](publishing-with-service-connection-points.md)                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Clase abstracta cuyas subclases usa el Servicio de nombres RPC (Ns) al que se accede a través de las **funciones RpcN de \*** la API win32. Para obtener más información, [vea Publicación con el servicio de nombres RPC (RPCN).](publishing-with-the-rpc-name-service-rpcns.md)                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Objeto de punto de conexión utilizado por el servicio de nombres de registro y resolución de sockets de Windows (RnR), al que se accede a través de las API de **WSA \*** Windows Sockets. Para obtener más información, [vea Publishing with Windows Sockets Registration and Resolution (RnR)](publishing-with-windows-sockets-registration-and-resolution.md)[Publicación con registro y resolución de sockets de Windows (RnR)]. |
| [**Printqueue**](/windows/desktop/ADSchema/c-printqueue)                         | Objeto de punto de conexión utilizado para publicar impresoras de red. Para obtener más información, [**vea IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**Volumen**](/windows/desktop/ADSchema/c-volume)                                 | Objeto de punto de conexión utilizado para publicar servicios de archivos.                                                                                                                                                                                                                                                                   |



 

Tenga en cuenta que los servicios basados en COM no usan objetos de punto de conexión para anunciarse. Estos servicios se publican en el almacén de clases. El Windows de clases 2000 es un repositorio basado en directorios para todas las aplicaciones, interfaces y API basadas en COM que proporcionan para la publicación y asignación de aplicaciones. Para obtener más información, [vea Publicación de servicios COM+.](publishing-com-services.md)

 

 