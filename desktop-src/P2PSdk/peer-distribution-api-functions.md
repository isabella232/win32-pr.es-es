---
description: El servicio de distribución del mismo nivel de Microsoft admite funciones tanto para el rol de consumidor como para los escenarios de rol de publicador.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funciones de la API de distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667410"
---
# <a name="peer-distribution-api-functions"></a>Funciones de la API de distribución del mismo nivel

El servicio de distribución del mismo nivel de Microsoft admite funciones tanto para el rol de consumidor como para los escenarios de rol de publicador.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Las siguientes funciones son comunes en los escenarios "cliente" y "servidor".



| Funciones comunes                                                                                       | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Crea una nueva instancia de **\_ \_ identificador de instancia de PEERDIST** que se debe pasar a todas las demás API de distribución del mismo nivel. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Libera los recursos asignados por la llamada a [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup).                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Devuelve el estado actual del servicio de distribución del mismo nivel.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Devuelve el estado actual y las capacidades del servicio de distribución del mismo nivel.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera los resultados de las operaciones asincrónicas.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Solicita que el servicio de distribución del mismo nivel notifique al llamador cuando se produce un cambio de estado.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Solicita que el servicio de distribución del mismo nivel notifique al llamador cuando se produce un cambio de estado.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Anula el registro de la notificación de cambio de estado para la sesión asociada al identificador proporcionado.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Las siguientes funciones solo se admiten en escenarios de "cliente".



| Funciones de cliente                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Abre y devuelve un **\_ \_ identificador de contenido de PEERDIST** para hacer referencia a ese contenido.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Cierra el **identificador de \_ contenido \_ de PEERDIST**.                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera información adicional del servicio de distribución del mismo nivel para un identificador de contenido específico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Agrega información de contenido que, a continuación, se asocia al **\_ \_ identificador de contenido de PEERDIST**. Un **\_ \_ identificador de contenido de PEERDIST** puede asociarse a cualquier información de contenido.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica el final de la información de contenido.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Se usa para proporcionar contenido a la memoria caché local. Normalmente esto se hace cuando no se encuentran datos en la red local, como se indica cuando [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) o [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) se completan con el **tiempo de \_ espera de error** o cuando **\_ \_ faltan \_ datos de error de PEERDIST**. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Proporciona acceso aleatorio a la secuencia de contenido.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Proporciona acceso secuencial a la secuencia de contenido.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Quita el contenido que se ha agregado previamente al sistema local de distribución del mismo nivel.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Cancela la operación asincrónica asociada a una estructura [superpuesta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) y el identificador de contenido devuelto por [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Las siguientes funciones solo se admiten en escenarios de "servidor".



| Funciones de servidor                                                                             | Descripción                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Crea el **\_ \_ identificador de flujo de PEERDIST** que se puede usar con [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) para crear información de contenido para la secuencia de contenido. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Agrega datos a la secuencia a la que hace referencia el identificador de la secuencia de PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Se llama para indicar que todos los datos se han agregado a la secuencia.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Cierra el identificador de la secuencia.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Anula la publicación del contenido publicado previamente en el servicio de distribución del mismo nivel.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Abre un **\_ \_ identificador de CONTENTINFO de PEERDIST** para el contenido publicado.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Abre un **\_ \_ identificador de CONTENTINFO de PEERDIST** para el contenido publicado.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera la información de contenido asociada al contenido publicado.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ \_Identificador de CONTENTINFO** abierto por [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Cancela la operación asincrónica asociada con el identificador de contenido y la estructura [superpuesta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .                                             |



 

 

 
