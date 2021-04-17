---
description: El tipo de dirección de dispositivo describe las formas de direccionamiento permitido en una dirección, como un número de teléfono o una dirección IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Tipo de dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678125"
---
# <a name="address-type"></a><span data-ttu-id="c8e69-103">Tipo de dirección</span><span class="sxs-lookup"><span data-stu-id="c8e69-103">Address Type</span></span>

<span data-ttu-id="c8e69-104">El tipo de dirección de dispositivo describe las formas de direccionamiento permitido en una dirección, como un número de teléfono o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="c8e69-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="c8e69-105">Un dispositivo determinado comprenderá uno o varios tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c8e69-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="c8e69-106">Para obtener una lista de tipos de direcciones compatibles con TAPI, vea [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8e69-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="c8e69-107">La [traducción de direcciones](initiate-a-session-ovr.md) se puede usar para convertir una dirección de un tipo a otro.</span><span class="sxs-lookup"><span data-stu-id="c8e69-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="c8e69-108">Para obtener información general sobre las direcciones, vea [Dirección](address-ovr.md) en [categorías de dispositivos](device-categories.md).</span><span class="sxs-lookup"><span data-stu-id="c8e69-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="c8e69-109">El [tipo de dirección de una sesión](address-type-for-a-session-ovr.md) será un subconjunto de los tipos de direcciones de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8e69-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="c8e69-110">**TAPI 2. x:** Vea [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) y el miembro **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="c8e69-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="c8e69-111">**TAPI 3. x:** Vea [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), con *AddressCap* establecido en el miembro **AC \_ ADDRESSTYPES** de [**la \_ funcionalidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span><span class="sxs-lookup"><span data-stu-id="c8e69-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
