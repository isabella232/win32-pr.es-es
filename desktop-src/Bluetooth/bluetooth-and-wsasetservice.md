---
title: Bluetooth y WSASetService
description: Bluetooth usa la función WSASetService para registrar o quitar una instancia de servicio en el espacio de nombres Bluetooth (NS \_ BTH) del registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Bluetooth de WSASetService
- Bluetooth y WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487786"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="cd8ad-106">Bluetooth y WSASetService</span><span class="sxs-lookup"><span data-stu-id="cd8ad-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="cd8ad-107">Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio en el espacio de nombres Bluetooth (NS \_ BTH) del registro.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="cd8ad-108">El identificador devuelto por esta operación solo se puede usar para eliminar el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="cd8ad-109">Bluetooth tiene dos formas de anunciar servicios mediante la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="cd8ad-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="cd8ad-110">La aplicación puede hacer que el sistema anuncie un registro del Servicio SDP Bluetooth simple, construido a partir de los miembros estándar de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="cd8ad-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="cd8ad-111">La aplicación puede hacer que el sistema anuncie su propio registro SDP Bluetooth pasando una estructura de [**\_ \_ servicio del conjunto BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) en el miembro **lpBlob** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="cd8ad-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="cd8ad-112">Se trata de un enfoque más complejo.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="cd8ad-113">Los registros SDP anunciados por [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) no se conservan después de que se cierre el proceso que los publicó.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="cd8ad-114">El uso de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth tiene los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="cd8ad-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="cd8ad-115">El parámetro *lpqsRegInfo* es la dirección de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="cd8ad-116">El parámetro *essOperation* es una enumeración que contiene una de las operaciones que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="cd8ad-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd8ad-117">Value</span></span>                  | <span data-ttu-id="cd8ad-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd8ad-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd8ad-119">registro de RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="cd8ad-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="cd8ad-120">Comienza a anunciar el servicio a las radios remotas que consultan mediante el protocolo SDP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="cd8ad-121">\_anular registro de RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="cd8ad-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="cd8ad-122">No es válido.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-122">Not valid.</span></span> <span data-ttu-id="cd8ad-123">Devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="cd8ad-124">RNRSERVICE \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="cd8ad-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="cd8ad-125">Deja de anunciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="cd8ad-126">Los identificadores de servicio detectados durante una llamada a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) son incompatibles con la operación de eliminación de RNRSERVICE \_ .</span><span class="sxs-lookup"><span data-stu-id="cd8ad-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="cd8ad-127">El parámetro *dwControlFlags* está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="cd8ad-128">Para obtener más información y una lista de opciones de Socket Bluetooth, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="cd8ad-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd8ad-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd8ad-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd8ad-130">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="cd8ad-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 