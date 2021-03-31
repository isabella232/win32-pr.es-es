---
description: Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que la información confidencial contenida en un evento no se ve comprometida.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Consideraciones de seguridad de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000843"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="db3c6-103">Consideraciones de seguridad de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="db3c6-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="db3c6-104">Al usar el servicio de eventos COM+, hay pasos que puede seguir para asegurarse de que la información confidencial contenida en un evento no se ve comprometida.</span><span class="sxs-lookup"><span data-stu-id="db3c6-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="db3c6-105">Los publicadores de eventos deben tener en cuenta que cualquier parte que pueda escribir en el catálogo de COM+ puede suscribirse a sus eventos.</span><span class="sxs-lookup"><span data-stu-id="db3c6-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="db3c6-106">Por consiguiente, si la información contenida en un objeto de clase de eventos es confidencial, debe utilizar la herramienta de administración de servicios de componentes para comprobar que las comunicaciones con los suscriptores están cifradas para la aplicación que contiene los componentes de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="db3c6-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="db3c6-107">(En la ficha **seguridad** de la hoja de propiedades de la aplicación com+, seleccione **privacidad de paquete** como el **nivel de autenticación para llamadas** ). Además, debe utilizar [filtros de eventos](filtering-events-in-com-.md) para asegurarse de que los eventos se entreguen solo a los suscriptores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="db3c6-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="db3c6-108">Los suscriptores de eventos deberían tener en cuenta que un usuario malintencionado con acceso a la red y el conocimiento del objeto de la clase de evento podría crear eventos falsos.</span><span class="sxs-lookup"><span data-stu-id="db3c6-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="db3c6-109">Por lo tanto, debe utilizar [la seguridad basada en roles](role-based-security-administration.md) para asegurarse de que los llamadores de los métodos del objeto de la clase de evento tienen las credenciales adecuadas para realizar las acciones descritas por su implementación.</span><span class="sxs-lookup"><span data-stu-id="db3c6-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="db3c6-110">Para ayudar a proteger a los publicadores y suscriptores, utilice el servicio de eventos COM+ en una red privada de hosts de confianza que está aislado de Internet por un firewall.</span><span class="sxs-lookup"><span data-stu-id="db3c6-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db3c6-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db3c6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db3c6-112">Seguridad de COM+</span><span class="sxs-lookup"><span data-stu-id="db3c6-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="db3c6-113">Filtrado de eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="db3c6-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="db3c6-114">Objeto de la clase de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="db3c6-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



