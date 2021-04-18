---
description: Cada línea tiene uno o más canales. Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requiere un conocimiento específico de los canales.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543006"
---
# <a name="channel-telephony-api"></a><span data-ttu-id="cefa2-104">Canal (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="cefa2-104">Channel (Telephony API)</span></span>

<span data-ttu-id="cefa2-105">Cada línea tiene uno o más canales.</span><span class="sxs-lookup"><span data-stu-id="cefa2-105">Each line has one or more channels.</span></span> <span data-ttu-id="cefa2-106">Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requiere un conocimiento específico de los canales.</span><span class="sxs-lookup"><span data-stu-id="cefa2-106">The service providers normally handle how channels are exposed as addresses to an application, and the end user or server does not require specific knowledge of channels.</span></span>

<span data-ttu-id="cefa2-107">Los canales son idénticos y, por tanto, intercambiables.</span><span class="sxs-lookup"><span data-stu-id="cefa2-107">Channels are identical and therefore interchangeable.</span></span> <span data-ttu-id="cefa2-108">En POTS (servicio telefónico anterior), hay exactamente un canal en una línea y el canal se usa exclusivamente para la voz.</span><span class="sxs-lookup"><span data-stu-id="cefa2-108">In POTS (Plain Old Telephone Service), exactly one channel exists on a line, and the channel is used exclusively for voice.</span></span> <span data-ttu-id="cefa2-109">Con ISDN, pueden existir al menos tres canales (y hasta un máximo de 30 o más) en una línea simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="cefa2-109">With ISDN, at least three (and as many as 30 or more) channels can exist on a line simultaneously.</span></span>

<span data-ttu-id="cefa2-110">Cada canal puede tener su propia dirección, lo que significa que una línea podría tener tantas direcciones como el número de canales.</span><span class="sxs-lookup"><span data-stu-id="cefa2-110">Each channel can have its own address, which means a line could have as many addresses as it has channels.</span></span> <span data-ttu-id="cefa2-111">La relación exacta entre los canales y las direcciones que se exponen a una aplicación depende de la implementación de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="cefa2-111">The precise relationship between channels and addresses exposed to an application is dependent on a service provider's implementation.</span></span>

<span data-ttu-id="cefa2-112">Algunos proveedores de servicios admiten la asignación de más de una dirección a un solo canal.</span><span class="sxs-lookup"><span data-stu-id="cefa2-112">Some service providers support the assignment of more than one address to a single channel.</span></span> <span data-ttu-id="cefa2-113">En las líneas de POTS, varios sistemas hacen posibles varias direcciones, como el marcado entrante directo (DID) o el timbre distintivo, que son servicios de tarifa adicional que proporciona la compañía telefónica.</span><span class="sxs-lookup"><span data-stu-id="cefa2-113">On POTS lines, multiple addresses are made possible by various systems, such as direct inward dialing (DID) or distinctive ringing, which are extra-fee services that the telephone company provides.</span></span>

<span data-ttu-id="cefa2-114">Muchas grandes corporaciones usan las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="cefa2-114">Many large corporations use DID for incoming calls.</span></span> <span data-ttu-id="cefa2-115">Antes de que una llamada esté conectada, su número de extensión de destino se señala a la PBX, lo que hace que la extensión suene en lugar del teléfono del operador.</span><span class="sxs-lookup"><span data-stu-id="cefa2-115">Before a call is connected, its destination extension number is signaled to the PBX, which causes the extension to ring instead of the operator's phone.</span></span> <span data-ttu-id="cefa2-116">Un ejemplo de timbre distintivo en un hogar privado sería si los elementos primarios usaban una dirección, los secundarios y una tercera.</span><span class="sxs-lookup"><span data-stu-id="cefa2-116">An example of distinctive ringing in a private home would be if the parents used one address, the children another, and a fax machine a third.</span></span> <span data-ttu-id="cefa2-117">Dado que solo una línea conecta la casa con la red telefónica, todos los teléfonos se conectan cuando aparece una llamada, pero el patrón de anillo es diferente en función del número marcado por la parte que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="cefa2-117">Because only one line connects the house to the telephone network, all phones ring when a call appears, but the ring pattern is different depending on the number that the calling party dialed.</span></span> <span data-ttu-id="cefa2-118">Con timbres distintivos, las personas saben quién es la llamada entrante y el equipo de fax responde a sus llamadas al reconocer su propio estilo de timbre.</span><span class="sxs-lookup"><span data-stu-id="cefa2-118">With distinctive ringing, the people know who the incoming call is for, and the fax machine answers its calls by recognizing its own ringing style.</span></span>

<span data-ttu-id="cefa2-119">En ISDN, es posible que los distintos canales B no tengan direcciones independientes.</span><span class="sxs-lookup"><span data-stu-id="cefa2-119">In ISDN, the various B channels might not have separate addresses.</span></span> <span data-ttu-id="cefa2-120">Dado que estos canales B pueden estar en la misma dirección, es el proveedor de servicios (y no la aplicación o la persona que ha marcado el número) que asigna llamadas a estos canales.</span><span class="sxs-lookup"><span data-stu-id="cefa2-120">Because these B channels might be on the same address, it is the service provider (and not the application or a person who has dialed the number) that assigns calls to these channels.</span></span>

 

 



