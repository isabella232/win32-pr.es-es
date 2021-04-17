---
description: Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificadores de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686635"
---
# <a name="address-identifiers"></a><span data-ttu-id="5cc11-103">Identificadores de direcciones</span><span class="sxs-lookup"><span data-stu-id="5cc11-103">Address Identifiers</span></span>

<span data-ttu-id="5cc11-104">Después de la asignación de direcciones, TAPI asigna identificadores de dirección a las direcciones.</span><span class="sxs-lookup"><span data-stu-id="5cc11-104">After address assignment, TAPI assigns address identifiers to the addresses.</span></span> <span data-ttu-id="5cc11-105">Un *identificador de dirección* es un número entre 0 y el número de direcciones de la línea menos uno.</span><span class="sxs-lookup"><span data-stu-id="5cc11-105">An *address identifier* is a number between 0 and the number of addresses on the line minus one.</span></span> <span data-ttu-id="5cc11-106">Un identificador de dirección es un número permanente asignado a un dispositivo determinado y permanece constante entre las actualizaciones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5cc11-106">An address identifier is a permanent number assigned to a given device and remains constant even across operating system upgrades.</span></span> <span data-ttu-id="5cc11-107">La combinación de [identificador de dispositivo](device-identifier-ovr.md) e identificador de dirección identifica de forma única una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="5cc11-107">The combination of [device identifier](device-identifier-ovr.md) and address identifier uniquely identifies a given address.</span></span>

<span data-ttu-id="5cc11-108">**TAPI 2. x:** Las aplicaciones obtienen un identificador de dirección (y un identificador de dispositivo) durante una llamada a [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), en la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) o en una llamada a [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span><span class="sxs-lookup"><span data-stu-id="5cc11-108">**TAPI 2.x:** Applications obtain an address identifier (and device identifier) during a call to [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) or [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure, or in a call to [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span></span>

<span data-ttu-id="5cc11-109">**TAPI 3. x:** El valor de [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) llamado *AddressCap* establecido en el miembro **AC \_ ADDRESSID** de la [**\_ funcionalidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) volverá con el parámetro *plCapability* establecido en el identificador de dirección actual.</span><span class="sxs-lookup"><span data-stu-id="5cc11-109">**TAPI 3.x:** The [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) called *AddressCap* set to the **AC\_ADDRESSID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) will return with the *plCapability* parameter set to the current address ID.</span></span>

 

 
