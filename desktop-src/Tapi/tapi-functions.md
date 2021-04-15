---
description: Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área. La información de cada función incluye una lista de los Estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Funciones de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545643"
---
# <a name="tapi-functions"></a><span data-ttu-id="c5f7e-104">Funciones de TAPI</span><span class="sxs-lookup"><span data-stu-id="c5f7e-104">TAPI Functions</span></span>

<span data-ttu-id="c5f7e-105">Las secciones siguientes contienen una lista alfabética de funciones agrupadas por área.</span><span class="sxs-lookup"><span data-stu-id="c5f7e-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="c5f7e-106">La información de cada función incluye una lista de los Estados de llamada válidos en la entrada de la función y las transiciones de estado de llamada típicas cuando se completa la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5f7e-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="c5f7e-107">Funciones de telefonía asistida</span><span class="sxs-lookup"><span data-stu-id="c5f7e-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="c5f7e-108">Funciones del centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="c5f7e-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="c5f7e-109">Funciones de dispositivo de línea</span><span class="sxs-lookup"><span data-stu-id="c5f7e-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="c5f7e-110">Funciones de dispositivo de teléfono</span><span class="sxs-lookup"><span data-stu-id="c5f7e-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="c5f7e-111">Para las funciones TAPI clasificadas por nivel de servicio y tarea, consulte [referencia rápida de funciones de TAPI](tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c5f7e-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="c5f7e-112">Tenga en cuenta que pueden existir limitaciones en el proveedor de servicios en relación con los Estados reales en los que se puede realizar una función.</span><span class="sxs-lookup"><span data-stu-id="c5f7e-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="c5f7e-113">Las aplicaciones deben comprobar el miembro **dwCallFeatures** de la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , el miembro **dwAddressFeatures** de la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) y el miembro **dwLineFeatures** de la estructura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para determinar si se permite una función dentro del estado de la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="c5f7e-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



