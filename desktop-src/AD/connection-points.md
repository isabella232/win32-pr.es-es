---
title: Puntos de conexión
description: Un objeto de punto de conexión contiene datos sobre una o varias instancias de un servicio disponible en la red.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- AD de puntos de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077553"
---
# <a name="connection-points"></a>Puntos de conexión

Un objeto de punto de conexión contiene datos sobre una o varias instancias de un servicio disponible en la red. La clase de objeto de conexión a todos es la clase base abstracta [**de la que**](/windows/desktop/ADSchema/c-connectionpoint) se derivan los objetos que representan recursos conectables en Active Directory Domain Services. En la ilustración siguiente se muestran algunas de las clases de objeto derivadas de la **clase de objeto de la imagen** .

![clases de objeto derivadas de la clase de objeto de tipo de objeto](images/connection-points.png)

En la tabla siguiente se enumeran las subclases inmediatas [**de la clase**](/windows/desktop/ADSchema/c-connectionpoint) de tipo de la.



| Clase de objeto                                                    | Descripción                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Objetos de punto de conexión de servicio (SCP) para publicar datos que usan las aplicaciones cliente para enlazar a un servicio. Para obtener más información, vea [publicar con puntos de conexión de servicio (SCP)](publishing-with-service-connection-points.md).                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Clase abstracta cuyas subclases se usan en el servicio de nombres RPC (NS) al que se tiene acceso a través de las funciones **RpcNs \*** de la API de Win32. Para obtener más información, vea [publicar con el servicio de nombres RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Objeto de punto de conexión utilizado por el servicio de nombres de registro y resolución de Windows Sockets (RnR), al que se tiene acceso a través de las API de Windows Sockets **WSA \*** . Para obtener más información, vea [publicar con el registro y la resolución de Windows Sockets (RNR)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**printQueue**](/windows/desktop/ADSchema/c-printqueue)                         | Objeto de punto de conexión usado para publicar impresoras de red. Para obtener más información, vea [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**cantidad**](/windows/desktop/ADSchema/c-volume)                                 | Objeto de punto de conexión usado para publicar servicios de archivo.                                                                                                                                                                                                                                                                   |



 

Tenga en cuenta que los servicios basados en COM no usan objetos de punto de conexión para anunciarse. Estos servicios se publican en el almacén de clases. El almacén de clases de Windows 2000 es un repositorio basado en directorios para todas las aplicaciones basadas en COM, interfaces y API que proporcionan para la publicación y la asignación de aplicaciones. Para obtener más información, vea [publicar servicios com+](publishing-com-services.md).

 

 