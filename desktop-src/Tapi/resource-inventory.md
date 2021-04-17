---
description: La aplicación debe realizar un inventario de los recursos de comunicaciones disponibles y, a continuación, notificar a TAPI los recursos que utilizará y cómo los usará.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677798"
---
# <a name="resource-inventory"></a><span data-ttu-id="1fc15-103">Inventario de recursos</span><span class="sxs-lookup"><span data-stu-id="1fc15-103">Resource Inventory</span></span>

<span data-ttu-id="1fc15-104">La aplicación debe realizar un inventario de los recursos de comunicaciones disponibles y, a continuación, notificar a TAPI los recursos que utilizará y cómo los usará.</span><span class="sxs-lookup"><span data-stu-id="1fc15-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="1fc15-105">Consulte [control de dispositivos](device-control.md) para obtener información adicional sobre los tipos de recursos y capacidades a los que puede tener acceso una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1fc15-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="1fc15-106">**TAPI 2. x:** Las aplicaciones obtienen el número de líneas disponibles cuando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) devuelve.</span><span class="sxs-lookup"><span data-stu-id="1fc15-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="1fc15-107">Después, pueden realizar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) en cada línea, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para cada dirección y [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) para cada línea que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1fc15-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="1fc15-108">**TAPI 3. x:** Las aplicaciones usan [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) o [**ITTAPI:: get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) para detectar las direcciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="1fc15-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="1fc15-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) y [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) proporcionan información sobre los tipos de comunicación posibles para cada dirección.</span><span class="sxs-lookup"><span data-stu-id="1fc15-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="1fc15-110">Si lo implementa el proveedor de servicios, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) proporciona a la aplicación acceso a información y controles adicionales.</span><span class="sxs-lookup"><span data-stu-id="1fc15-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
