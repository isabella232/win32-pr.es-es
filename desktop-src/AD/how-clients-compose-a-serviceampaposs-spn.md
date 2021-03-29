---
title: Cómo los clientes componen el SPN de un servicio
description: Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que se debe conectar.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Cómo los clientes componen el SPN de un servicio en AD
- nombre de entidad de seguridad de servicio AD, cómo los clientes componen el SPN de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993897"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="54cd3-105">Cómo los clientes componen el SPN de un servicio</span><span class="sxs-lookup"><span data-stu-id="54cd3-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="54cd3-106">Para autenticar un servicio, una aplicación cliente crea un SPN para la instancia de servicio a la que se debe conectar.</span><span class="sxs-lookup"><span data-stu-id="54cd3-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="54cd3-107">La aplicación cliente puede usar la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN.</span><span class="sxs-lookup"><span data-stu-id="54cd3-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="54cd3-108">El cliente especifica los componentes del SPN con datos conocidos o datos recuperados de orígenes distintos del propio servicio.</span><span class="sxs-lookup"><span data-stu-id="54cd3-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="54cd3-109">La forma de un SPN es como se muestra en el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="54cd3-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="54cd3-110">En este formato, &lt; &gt; se requiere "clase de servicio" y " &lt; host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="54cd3-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="54cd3-111">" &lt; Puerto &gt; " y " &lt; nombre de servicio &gt; " opcional.</span><span class="sxs-lookup"><span data-stu-id="54cd3-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="54cd3-112">Normalmente, el cliente reconoce la &lt; parte "clase &gt; de servicio" del nombre y reconoce los componentes opcionales que se van a incluir en el SPN.</span><span class="sxs-lookup"><span data-stu-id="54cd3-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="54cd3-113">El cliente puede recuperar componentes del SPN de orígenes como un punto de conexión de servicio (SCP) o una entrada de usuario.</span><span class="sxs-lookup"><span data-stu-id="54cd3-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="54cd3-114">Por ejemplo, el cliente puede leer el atributo **serviceDNSName** del SCP de un servicio para obtener el &lt; componente "host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="54cd3-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="54cd3-115">El atributo **serviceDNSName** contiene el nombre DNS del servidor en el que se ejecuta la instancia de servicio o el nombre DNS de los registros SRV que contienen los datos de host para las réplicas de servicio.</span><span class="sxs-lookup"><span data-stu-id="54cd3-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="54cd3-116">El &lt; componente "nombre del servicio &gt; ", que solo se usa para los servicios replicables, puede ser el nombre distintivo del SCP del servicio, el nombre DNS del dominio atendido por el servicio o el nombre DNS de los registros SRV o mx.</span><span class="sxs-lookup"><span data-stu-id="54cd3-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="54cd3-117">Para obtener más información y un ejemplo de código que se usa para crear un SPN para un servicio, vea [cómo un cliente autentica un servicio de Windows Sockets basado en SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="54cd3-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="54cd3-118">Para obtener más información y una descripción de los componentes de SPN, vea [formatos de nombre para SPN únicos](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="54cd3-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




