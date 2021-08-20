---
description: La API de distribución del mismo nivel, que admite la característica de caché de ramas en Windows 7, Windows Server 2008 R2, Windows 8 y Windows Server 2012 ofrece un conjunto de API de plataforma que pueden aumentar la capacidad de respuesta de la red de las aplicaciones centralizadas cuando se accede desde oficinas remotas y ayudar a reducir el uso general de la red de área extensa (WAN) sin interferir con las tecnologías de seguridad de red.
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Acerca de la distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11085b38819f8b102f71f59294924c7c6e079881c8af87f77923351ff424f959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553485"
---
# <a name="about-peer-distribution"></a>Acerca de la distribución del mismo nivel

La API de distribución del mismo nivel, que admite la característica de caché de ramas en Windows 7, Windows Server 2008 R2, Windows 8 y Windows Server 2012 ofrece un conjunto de API de plataforma que pueden aumentar la capacidad de respuesta de la red de las aplicaciones centralizadas cuando se accede desde oficinas remotas y ayudar a reducir el uso general de la red de área extensa (WAN) sin interferir con las tecnologías de seguridad de red.

El sistema de distribución del mismo nivel ofrece un conjunto de API de plataforma que usan los publicadores que proporcionan contenido digital y los consumidores que lo solicitan. Para diferenciar fácilmente estos roles, puede ser más fácil pensar en el publicador en un rol de servidor y en el consumidor en un rol de cliente. Además, es importante recordar que, aparte de estos roles conceptuales, el servicio de distribución del mismo nivel es un verdadero sistema del mismo nivel, como se indica en la capacidad de cualquier nodo de distribución del mismo nivel de publicar y consumir contenido digital. Las API de la plataforma de distribución del mismo nivel se exponen a publicadores y consumidores mediante una biblioteca de importación de Win32 **(PeerDist.Lib**).

El ciclo de vida del contenido proporcionado por un publicador y recuperado por un consumidor con el servicio de distribución del mismo nivel se compone de las siguientes operaciones:



|                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Publicación de contenido** | La publicación se realiza para generar una descripción del contenido que se denomina **Información** de contenido o Información **de contenido** para abrirla. A continuación, una instancia del servicio de distribución del mismo nivel puede usar esta información de contenido para autenticar y volver a generar el contenido. Cuando una aplicación publica contenido en el servicio de distribución del mismo nivel, que conceptualmente es una operación del lado servidor, ese contenido se asocia a la identidad de Publisher, que se basa en el SID del usuario asociado al token de acceso de subproceso. Este enlace se realiza para limitar el acceso al contenido por entidades no autorizadas. Sin embargo, es importante tener en cuenta que el acceso a la información de contenido es equivalente al acceso al propio contenido, ya que la información de contenido se puede usar para obtener el contenido de elementos del mismo nivel o de una caché hospedada.<br/> Hay una nueva versión de la estructura de datos de información de contenido en Windows 8; sin embargo, todavía se admite la versión anterior. Para interoperar con Windows 7 clientes, un administrador puede configurar el servicio de distribución del mismo nivel para usar la versión anterior de la estructura de datos de información de contenido.<br/> |
| **Recuperación de contenido**   | Para que un consumidor recupere contenido del servicio de distribución del mismo nivel, se debe proporcionar acceso a la información de contenido publicada asociada a ese contenido. El servicio de distribución del mismo nivel que se usa para publicar el contenido puede proporcionar la información de contenido asociada. Una vez que el consumidor tiene la información de contenido, se pueden usar otras API de distribución del mismo nivel para solicitar contenido del servicio de distribución del mismo nivel. El servicio de distribución del mismo nivel intentará recuperar el contenido de la red local. Si el contenido no está disponible, la aplicación cliente es responsable de recuperar el contenido del servidor de origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Eliminación de publicaciones** | En el caso de las aplicaciones que han publicado contenido en el servicio de distribución del mismo nivel, se ha proporcionado la función [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) para permitir que el contenido no se publique. Una vez que el contenido se ha dejado de publicar, el servicio de distribución del mismo nivel local ya no proporcionará la información de contenido asociada a ese contenido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Finalizaciones asincrónicas

La API de distribución del mismo nivel admite un modelo de API asincrónico y, como resultado, las API de distribución del mismo nivel permiten el uso de puertos o eventos de finalización de E/S como mecanismos de señalización para procesar finalizaciones asincrónicas de operaciones de distribución del mismo nivel. Para cualquiera de los mecanismos, distribución del mismo nivel usa [**una estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) En general, distribución del mismo nivel toma la propiedad de una estructura **OVERLAPPED** y los parámetros out que el cliente pasa a las funciones de API asincrónicas. El cliente no debe tener acceso a estos recursos hasta que se complete la función asincrónica concreta. Tan pronto como se completen las funciones asincrónicas, el servicio de distribución del mismo nivel ya no requerirá acceso a estos recursos y se pueden reutilizar según la aplicación que realiza la llamada.

No habrá ninguna finalización asincrónica si la función devuelve cualquier código de error distinto de **ERROR \_ E/S \_ PENDIENTE.** La devolución de un valor distinto de **ERROR \_ IO \_ PENDING** significa que la llamada ha producido un error sincrónicamente. Si la API de distribución del mismo nivel devuelve **ERROR \_ \_ E/S PENDIENTE,** el autor de la llamada debe esperar a la finalización asincrónica.

El código de error de la finalización asincrónica se puede recuperar de una de estas dos maneras:

**Finalización basada en puertos de finalización de E/S**

El usuario invoca el mecanismo de puerto de finalización de E/S proporcionando un identificador de puerto de finalización y una clave de finalización a las siguientes funciones de API:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

El usuario crea un puerto de finalización mediante una [**llamada a CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Este identificador de puerto de finalización se puede usar simultáneamente para otras operaciones de E/S asincrónicas, así como para operaciones específicas de distribución del mismo nivel.

El autor de la llamada [**debe usar la función GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para administrar la finalización asincrónica. Si se produce un error en la operación asincrónica, la función **GetQueuedCompletionStatus** devolverá **FALSE** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error adecuado. El autor de la llamada debe omitir todos los campos de la [**estructura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) si el código de error es distinto de **ERROR \_ SUCCESS**. La operación asincrónica se realiza correctamente **si la función GetQueuedCompletionStatus** devuelve **TRUE.**

Para obtener más información, vea [Puertos de finalización de E/S.](/windows/desktop/FileIO/i-o-completion-ports)

**Finalización basada en eventos**

Si el autor de la llamada establece un identificador de evento válido en el campo *hEvent* de la estructura [**OVERLAPPED,**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) distribución del mismo nivel lo usa para indicar que se ha completado la operación de E/S asincrónica asociada.

Un llamador de subproceso puede administrar operaciones superpuestas especificando un identificador para el objeto de evento de restablecimiento manual de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en una de las funciones de espera. Una vez señalado el evento, el autor de la llamada debe llamar a [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) pasando la estructura **OVERLAPPED** adecuada. **PeerGetOverlappedResult** devolverá **FALSE** y el autor de la llamada debe llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el código de error. El autor de la llamada debe omitir todos los campos de la **estructura OVERLAPPED** si el código de error es distinto de **ERROR \_ SUCCESS**. La operación asincrónica se realiza correctamente **si la función PeerGetOverlappedResult** devuelve **TRUE**.

Si el autor de la llamada proporciona un puerto de finalización junto con un evento, el evento se usará como mecanismo de finalización.

**Windows 7:** Use la [**función GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) en lugar de [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de distribución del mismo nivel](peer-distribution-api-reference.md)
</dt> </dl>

 

