---
description: A continuación se muestra la funcionalidad de la interfaz ITConnection.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaz ITConnection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681140"
---
# <a name="itconnection-interface"></a><span data-ttu-id="0e713-103">Interfaz ITConnection</span><span class="sxs-lookup"><span data-stu-id="0e713-103">ITConnection interface</span></span>

<span data-ttu-id="0e713-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e713-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e713-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0e713-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0e713-106">La interfaz **ITConnection** proporciona la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="0e713-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="0e713-107">Proporciona acceso a la información de la dirección y el período de vida (TTL) de la sesión.</span><span class="sxs-lookup"><span data-stu-id="0e713-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="0e713-108">Proporciona acceso a la información de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="0e713-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="0e713-109">Habilita la manipulación de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="0e713-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="0e713-110">La interfaz **ITConnection** se crea llamando a **QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="0e713-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="0e713-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e713-111">Members</span></span>

<span data-ttu-id="0e713-112">La interfaz **ITConnection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0e713-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0e713-113">**ITConnection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0e713-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="0e713-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0e713-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e713-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0e713-115">Methods</span></span>

<span data-ttu-id="0e713-116">La interfaz **ITConnection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0e713-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="0e713-117">Método</span><span class="sxs-lookup"><span data-stu-id="0e713-117">Method</span></span>                                                               | <span data-ttu-id="0e713-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e713-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e713-119">**obtener \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="0e713-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="0e713-120">Obtiene el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="0e713-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0e713-121">**obtener \_ ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="0e713-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="0e713-122">Obtiene el valor de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="0e713-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0e713-123">**obtener \_ BandwidthModifier**</span><span class="sxs-lookup"><span data-stu-id="0e713-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="0e713-124">Obtiene el modificador de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="0e713-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0e713-125">**obtener \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="0e713-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="0e713-126">Obtiene el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="0e713-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0e713-127">**obtener \_ NumAddresses**</span><span class="sxs-lookup"><span data-stu-id="0e713-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="0e713-128">Obtiene el número de direcciones que se van a utilizar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="0e713-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="0e713-129">**obtener \_ StartAddress**</span><span class="sxs-lookup"><span data-stu-id="0e713-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="0e713-130">Obtiene la primera dirección que se va a utilizar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="0e713-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0e713-131">**obtener \_ TTL**</span><span class="sxs-lookup"><span data-stu-id="0e713-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="0e713-132">Obtiene el ámbito del [*período*](t-tapgloss.md) de vida (TTL) para las transmisiones en las direcciones.</span><span class="sxs-lookup"><span data-stu-id="0e713-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="0e713-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="0e713-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="0e713-134">Obtiene la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="0e713-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="0e713-135">**Put \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="0e713-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="0e713-136">Establece el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="0e713-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0e713-137">**Put \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="0e713-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="0e713-138">Establece el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="0e713-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0e713-139">**SetAddressInfo**</span><span class="sxs-lookup"><span data-stu-id="0e713-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="0e713-140">Establece la información de dirección.</span><span class="sxs-lookup"><span data-stu-id="0e713-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0e713-141">**SetBandwidthInfo**</span><span class="sxs-lookup"><span data-stu-id="0e713-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="0e713-142">Establece el valor de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="0e713-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0e713-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="0e713-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="0e713-144">Establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.</span><span class="sxs-lookup"><span data-stu-id="0e713-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="0e713-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e713-145">Requirements</span></span>



| <span data-ttu-id="0e713-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e713-146">Requirement</span></span> | <span data-ttu-id="0e713-147">Value</span><span class="sxs-lookup"><span data-stu-id="0e713-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e713-148">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0e713-148">TAPI version</span></span><br/> | <span data-ttu-id="0e713-149">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0e713-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0e713-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e713-150">Header</span></span><br/>       | <dl> <span data-ttu-id="0e713-151"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e713-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e713-152">Library</span></span><br/>      | <dl> <span data-ttu-id="0e713-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0e713-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e713-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="0e713-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e713-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

