---
description: Las funciones de telefonía extendidas se enumeran por Categoría en las tablas siguientes.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referencia de servicios de telefonía extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677380"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="2df21-103">Referencia de servicios de telefonía extendidos</span><span class="sxs-lookup"><span data-stu-id="2df21-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="2df21-104">Las funciones de telefonía extendidas se enumeran por Categoría en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2df21-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="2df21-105">Funciones de telefonía extendidas para dispositivos de línea</span><span class="sxs-lookup"><span data-stu-id="2df21-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="2df21-106">Función</span><span class="sxs-lookup"><span data-stu-id="2df21-106">Function</span></span>                                                   | <span data-ttu-id="2df21-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2df21-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2df21-108">**lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="2df21-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="2df21-109">Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="2df21-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="2df21-110">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="2df21-110">Asynchronous.</span></span> |
| [<span data-ttu-id="2df21-111">**lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="2df21-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="2df21-112">Proporciona a los proveedores de servicios acceso a características específicas del dispositivo no ofrecidas por otras funciones TAPI.</span><span class="sxs-lookup"><span data-stu-id="2df21-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="2df21-113">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2df21-113">Synchronous.</span></span> |
| [<span data-ttu-id="2df21-114">**lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="2df21-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="2df21-115">Envía características de conmutador específicas del dispositivo al conmutador.</span><span class="sxs-lookup"><span data-stu-id="2df21-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="2df21-116">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="2df21-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="2df21-117">Funciones de telefonía extendidas para dispositivos telefónicos</span><span class="sxs-lookup"><span data-stu-id="2df21-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="2df21-118">Función</span><span class="sxs-lookup"><span data-stu-id="2df21-118">Function</span></span>                                                     | <span data-ttu-id="2df21-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2df21-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2df21-120">**phoneDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="2df21-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="2df21-121">Función de escape específica del dispositivo para permitir las extensiones dependientes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2df21-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="2df21-122">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="2df21-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="2df21-123">**PhoneNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="2df21-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="2df21-124">Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo de teléfono especificado.</span><span class="sxs-lookup"><span data-stu-id="2df21-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="2df21-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2df21-125">Synchronous.</span></span> |



 

 

 



