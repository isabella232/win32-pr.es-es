---
description: El servicio Distribución del mismo nivel de Microsoft admite funciones para escenarios de rol de consumidor y de rol de publicador.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funciones de la API de distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069214"
---
# <a name="peer-distribution-api-functions"></a>Funciones de la API de distribución del mismo nivel

El servicio Distribución del mismo nivel de Microsoft admite funciones para escenarios de rol de consumidor y de rol de publicador.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Las siguientes funciones son comunes en escenarios de "cliente" y "servidor".



| Funciones comunes                                                                                       | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Crea una nueva **instancia de PEERDIST \_ INSTANCE \_ HANDLE** que se debe pasar a todas las demás API de distribución del mismo nivel. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Libera los recursos asignados por la llamada a [**PeerDistStartup.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Devuelve el estado actual del servicio de distribución del mismo nivel.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Devuelve el estado actual y las funcionalidades del servicio de distribución del mismo nivel.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera los resultados de las operaciones asincrónicas.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Solicita que el servicio de distribución del mismo nivel notifique al autor de la llamada cuando se produce un cambio de estado.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Solicita que el servicio de distribución del mismo nivel notifique al autor de la llamada cuando se produce un cambio de estado.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Anula el registro de la notificación de cambio de estado de la sesión asociada al identificador proporcionado.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Las siguientes funciones solo se admiten en escenarios de "cliente".



| Funciones de cliente                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Abre y devuelve un **IDENTIFICADOR DE CONTENIDO DE PEERDIST \_ \_** para hacer referencia a ese contenido.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Cierra el IDENTIFICADOR **DE CONTENIDO \_ DE \_ PEERDIST.**                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera información adicional del servicio de distribución del mismo nivel para un identificador de contenido específico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Agrega información de contenido que, a continuación, está asociada al **IDENTIFICADOR DE CONTENIDO \_ DE \_ PEERDIST.** Un **IDENTIFICADOR DE CONTENIDO DE PEERDIST \_ \_** se puede asociar a cualquier información de contenido.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica el final de la información de contenido.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Se usa para proporcionar contenido a la memoria caché local. Normalmente, esto se hace cuando no se pueden encontrar datos en la red local como se indica cuando [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) o [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) se completan con **ERROR \_ TIMEOUT** o **PEERDIST \_ ERROR MISSING \_ \_ DATA**.. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Proporciona acceso aleatorio al flujo de contenido.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Proporciona acceso secuencial al flujo de contenido.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Quita el contenido que se ha agregado previamente al sistema de distribución del mismo nivel local.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Cancela la operación asincrónica asociada a una [estructura OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) y al identificador de contenido devuelto [**por PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Las siguientes funciones solo se admiten en escenarios de "servidor".



| Funciones de servidor                                                                             | Descripción                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Crea el **IDENTIFICADOR DE FLUJO DE PEERDIST \_ \_** que se puede usar [**con PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) para crear información de contenido para el flujo de contenido. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Agrega datos a la secuencia a la que hace referencia el identificador de flujo PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Se llama para indicar que se han agregado todos los datos a la secuencia.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Cierra el identificador de flujo.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Despublica el contenido publicado previamente en el servicio distribución del mismo nivel.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Abre un **IDENTIFICADOR CONTENTINFO de PEERDIST \_ \_** para el contenido publicado.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Abre un **IDENTIFICADOR CONTENTINFO de PEERDIST \_ \_** para el contenido publicado.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera la información de contenido asociada al contenido publicado.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ IDENTIFICADOR DE \_ CONTENTINFO** abierto [**por PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Cancela la operación asincrónica asociada con el identificador de contenido y [la estructura OVERLAPPED.](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)                                             |



 

 

 
