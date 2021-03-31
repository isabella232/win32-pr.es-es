---
description: El reenvío es la desviación de una sesión entrante en una dirección de destino diferente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Adelante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907975"
---
# <a name="forward"></a><span data-ttu-id="c04fb-103">Adelante</span><span class="sxs-lookup"><span data-stu-id="c04fb-103">Forward</span></span>

<span data-ttu-id="c04fb-104">El reenvío es la desviación de una sesión entrante en una dirección de destino diferente.</span><span class="sxs-lookup"><span data-stu-id="c04fb-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="c04fb-105">TAPI permite que una aplicación especifique una lista de condiciones de reenvío para una dirección.</span><span class="sxs-lookup"><span data-stu-id="c04fb-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="c04fb-106">Las condiciones de reenvío pueden ser tan precisas como un modo de destino y [**reenvío**](./lineforwardmode--constants.md) diferente para cada dirección del llamador.</span><span class="sxs-lookup"><span data-stu-id="c04fb-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="c04fb-107">La operación de reenvío también se puede usar para implementar una característica de acción de no molestar selectiva, reenviando algunos autores de llamadas al correo de voz y permitiendo que otros intenten finalizar.</span><span class="sxs-lookup"><span data-stu-id="c04fb-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="c04fb-108">La operación de reenvío también puede cancelar cualquier reenvío que esté actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="c04fb-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="c04fb-109">Algunos proveedores de servicios requieren que una aplicación cree una llamada de consulta antes de una operación de reenvío.</span><span class="sxs-lookup"><span data-stu-id="c04fb-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="c04fb-110">A continuación, se pasa a la operación de reenvío un puntero a la llamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="c04fb-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="c04fb-111">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="c04fb-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="c04fb-112">**TAPI 2. x:** Para establecer [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) para obtener [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), cambie la [**línea \_ ADDRESSSTATE**](./line-addressstate.md) mensaje de notificación con LINEADDRESSSTATE \_ forward.</span><span class="sxs-lookup"><span data-stu-id="c04fb-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="c04fb-113">**TAPI 3. x:** Vea [**ITAddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**ITADDRESSEVENT:: get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ forward.</span><span class="sxs-lookup"><span data-stu-id="c04fb-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="c04fb-114">Puede ser imposible que un proveedor de servicios sepa en todo momento qué reenvío está en vigor para una dirección.</span><span class="sxs-lookup"><span data-stu-id="c04fb-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="c04fb-115">El reenvío se puede cancelar o cambiar de maneras que no producen notificaciones al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c04fb-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
