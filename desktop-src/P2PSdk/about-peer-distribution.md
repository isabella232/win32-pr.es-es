---
description: La API de distribución del mismo nivel, que admite la característica de la caché de rama en Windows 7, Windows Server 2008 R2, Windows 8 y Windows Server 2012 ofrecen un conjunto de API de plataforma que pueden aumentar la capacidad de respuesta de la red de las aplicaciones centralizadas cuando se tiene acceso desde las oficinas remotas y como ayuda para reducir la utilización general de la red de área extensa
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Acerca de la distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b9a99a65ea2cfda6dc8ad9accd4d881529e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909798"
---
# <a name="about-peer-distribution"></a>Acerca de la distribución del mismo nivel

La API de distribución del mismo nivel, que admite la característica de la caché de rama en Windows 7, Windows Server 2008 R2, Windows 8 y Windows Server 2012 ofrecen un conjunto de API de plataforma que pueden aumentar la capacidad de respuesta de la red de las aplicaciones centralizadas cuando se tiene acceso desde las oficinas remotas y como ayuda para reducir la utilización general de la red de área extensa

El sistema de distribución del mismo nivel ofrece un conjunto de API de plataforma que usan tanto los publicadores que proporcionan contenido digital como los consumidores que lo solicitan. Para diferenciar fácilmente estos roles, puede ser más fácil pensar en el publicador en un rol de servidor y en el consumidor en un rol de cliente. Además, es importante recordar que, aparte de estos roles conceptuales, el servicio de distribución del mismo nivel es un sistema del mismo nivel, como se indica en la capacidad de cualquier nodo de distribución del mismo nivel para publicar y consumir contenido digital. Las API de la plataforma de distribución del mismo nivel se exponen a los publicadores y consumidores mediante una biblioteca de importación de Win32 (**PeerDist. lib**).

El ciclo de vida del contenido proporcionado por un publicador y recuperado por un consumidor con el servicio de distribución del mismo nivel se compone de las siguientes operaciones:



|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Publicación de contenido** | La publicación se realiza para generar una descripción de la **información** de contenido con términos de contenido, o información de **contenido** para abreviar. Esta información de contenido puede ser utilizada por una instancia del servicio de distribución del mismo nivel para autenticar y volver a generar el contenido. Cuando una aplicación publica el contenido en el servicio de distribución del mismo nivel, que es conceptualmente una operación del lado servidor, el contenido se asocia con la identidad del publicador, que se basa en el SID del usuario asociado al token de acceso del subproceso. Este enlace se realiza para limitar el acceso al contenido por parte de entidades no autorizadas. Sin embargo, es importante tener en cuenta que el acceso a la información de contenido es equivalente a acceder al contenido en sí, ya que la información de contenido puede usarse para obtener el contenido de los elementos del mismo nivel o de una caché hospedada.<br/> Hay una nueva versión de la estructura de datos de información de contenido en Windows 8. sin embargo, todavía se admite la versión anterior. Para interoperar con los clientes de Windows 7, un administrador puede configurar el servicio de distribución del mismo nivel para usar la versión anterior de la estructura de datos de información de contenido.<br/> |
| **Recuperación de contenido**   | Para que un consumidor recupere contenido del servicio de distribución del mismo nivel, se debe proporcionar acceso a la información de contenido publicada asociada a ese contenido. El servicio de distribución del mismo nivel que se usa para publicar el contenido puede proporcionar la información de contenido asociada. Una vez que el consumidor tiene la información de contenido, se pueden usar otras API de distribución del mismo nivel para solicitar contenido del servicio de distribución del mismo nivel. El servicio de distribución del mismo nivel intentará recuperar el contenido de la red local. Si el contenido no está disponible, la aplicación cliente es responsable de recuperar el contenido del servidor de origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Eliminación de publicaciones** | En el caso de las aplicaciones que han publicado contenido en el servicio de distribución del mismo nivel, se ha proporcionado la función [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) para permitir que el contenido no se publique. Una vez que se ha anulado la publicación del contenido, el servicio de distribución del mismo nivel local ya no proporcionará la información de contenido asociada a ese contenido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Finalizaciones asincrónicas

La API de distribución del mismo nivel admite un modelo de API asincrónica y, como resultado, las API de distribución del mismo nivel permiten el uso de eventos o puertos de finalización de e/s como mecanismos de señalización para procesar las finalizaciones asincrónicas de la operación de distribución del mismo nivel. En ambos mecanismos, la distribución del mismo nivel utiliza una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . En general, la distribución del mismo nivel toma la propiedad de una estructura **superpuesta** y los parámetros out que el cliente pasa a las funciones de API asincrónicas. El cliente no debe tener acceso a estos recursos hasta que se complete la función asincrónica concreta. En cuanto se completen las funciones asincrónicas, el servicio de distribución del mismo nivel ya no necesitará acceso a estos recursos y se pueden volver a usar cuando la aplicación que realiza la llamada sea apta.

No habrá ninguna finalización asincrónica si la función devuelve un código de error distinto del **error de \_ e/s \_ pendiente**. La devolución de un valor distinto del **error de \_ e/s \_ pendiente** significa que la llamada no se ha realizado de forma sincrónica. Si la API de distribución del mismo nivel devuelve un **error de \_ e/s \_ pendiente**, el autor de la llamada debe esperar la finalización asincrónica.

El código de error de la finalización asincrónica se puede recuperar de una de estas dos maneras:

**Finalización basada en Puerto de finalización de e/s**

El usuario invoca el mecanismo de puertos de finalización de e/s proporcionando un identificador de puerto de finalización y una clave de finalización a las siguientes funciones de API:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

El usuario crea un puerto de finalización mediante una llamada a [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Este identificador de puerto de finalización se puede usar simultáneamente para otras operaciones de e/s asincrónicas, así como operaciones específicas de distribución del mismo nivel.

El autor de la llamada debe usar la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para administrar la finalización asincrónica. Si se produce un error en la operación asincrónica, la función **GetQueuedCompletionStatus** devolverá **false** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error correspondiente. El autor de la llamada debe omitir todos los campos de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) si el código de error no es **\_ correcto**. La operación asincrónica se realiza correctamente si la función **GetQueuedCompletionStatus** devuelve **true**.

Para obtener más información [, vea puertos de finalización de e/s](/windows/desktop/FileIO/i-o-completion-ports).

**Finalización basada en eventos**

Si el autor de la llamada establece un identificador de evento válido para el campo *hEvent* de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , la distribución del mismo nivel lo usa para indicar que se ha completado la operación de e/s asincrónica asociada.

Un llamador de subproceso puede administrar las operaciones superpuestas especificando un identificador para el objeto de evento de restablecimiento manual de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en una de las funciones de espera. Una vez señalado el evento, el llamador debe llamar a [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) pasando la estructura **superpuesta** adecuada. **PeerGetOverlappedResult** devolverá **false** y el llamador debe llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error. El autor de la llamada debe omitir todos los campos de la estructura **superpuesta** si el código de error no es **\_ correcto**. La operación asincrónica se realiza correctamente si la función **PeerGetOverlappedResult** devuelve **true**.

Si el autor de la llamada proporciona un puerto de finalización junto con un evento, el evento se usará como mecanismo de finalización.

**Windows 7:** Use la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) en lugar de [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de distribución del mismo nivel](peer-distribution-api-reference.md)
</dt> </dl>

 

