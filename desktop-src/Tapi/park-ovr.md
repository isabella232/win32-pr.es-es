---
description: La operación de estacionamiento permite a una aplicación enviar una sesión a una dirección especial en la que se conservará hasta que se haya desactivado.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Aparcamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677939"
---
# <a name="park"></a><span data-ttu-id="0bbdc-103">Aparcamiento</span><span class="sxs-lookup"><span data-stu-id="0bbdc-103">Park</span></span>

<span data-ttu-id="0bbdc-104">La operación de estacionamiento permite a una aplicación enviar una sesión a una dirección especial en la que se conservará hasta que se haya desactivado.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="0bbdc-105">Desde el punto de vista de la aplicación, esto se parece mucho a una transferencia.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="0bbdc-106">Para la entidad en el otro extremo de la conexión, esto se asemeja a poner en espera.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="0bbdc-107">La diferencia entre estacionamiento y transferencia es que la dirección deestacionada no es un punto de conexión para la sesión y la sesión no alerta ni agota el tiempo de espera. La diferencia entre estacionamiento y Hold es que una vez finalizada la operación de estacionamiento, la sesión ya no está asociada a la dirección de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="0bbdc-108">Se proporcionan dos formas de estacionamiento de una sesión: estacionamiento *dirigido* y no *Redirigido*.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="0bbdc-109">En el parque de llamadas dirigidas, la aplicación especifica la dirección de destino en la que se va a detener la llamada.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="0bbdc-110">Con estacionamiento no directo, el proveedor de servicios o el hardware subyacente determinan la dirección y la devuelven a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="0bbdc-111">Una sesión aparcada normalmente entra en el estado de inactividad después de haberse detenido correctamente y, a continuación, la aplicación debe liberar los recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="0bbdc-112">Vea [finalizar una sesión](terminate-a-session-ovr.md) para obtener un resumen de cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="0bbdc-113">Si la aplicación se desactivará la sesión, se asignarán nuevos recursos de la sesión, incluso si la aplicación ha devuelto los punteros anteriores, por lo que si no se realizan las versiones adecuadas, se pueden producir diversos problemas.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="0bbdc-114">Algunos proveedores de servicios pueden recordar al usuario una vez que se ha detenido una sesión durante un período de tiempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="0bbdc-115">La aplicación ve una llamada de oferta con un [motivo](reason-ovr.md) de llamada establecido en recordatorio.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="0bbdc-116">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="0bbdc-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="0bbdc-117">**TAPI 2. x:** Vea [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="0bbdc-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="0bbdc-118">**TAPI 3:** Vea [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="0bbdc-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
