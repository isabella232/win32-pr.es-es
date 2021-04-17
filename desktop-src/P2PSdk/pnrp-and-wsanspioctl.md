---
description: PNRP usa la función WSANSPIoctl para recibir notificaciones acerca de los cambios realizados en lo siguiente.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP y WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667390"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="b3eb0-103">PNRP y WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="b3eb0-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="b3eb0-104">PNRP usa la función [**WSANSPIoctl**](winsock-nsp-reference-links.md) para recibir notificaciones acerca de los cambios realizados en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b3eb0-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="b3eb0-105">Una lista de nubes de red</span><span class="sxs-lookup"><span data-stu-id="b3eb0-105">A network cloud list</span></span>
-   <span data-ttu-id="b3eb0-106">Disponibilidad de los resultados de una solicitud de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="b3eb0-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="b3eb0-107">La primera llamada a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define el tipo de información sobre el que se notifica a un cliente.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="b3eb0-108">Se puede notificar a un cliente con un mensaje de Windows, una rutina de finalización, un identificador de un objeto WSAEVENT o un puerto.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="b3eb0-109">Para obtener más información sobre las opciones y el establecimiento del parámetro *lpCompletion* , consulte **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="b3eb0-110">Para seguir recibiendo notificaciones después de una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md), una aplicación debe llamar de nuevo a **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b3eb0-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="b3eb0-111">La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloquea incluso si se llama a **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b3eb0-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="b3eb0-112">Antes de llamar a **WSALookupServiceNext**, una aplicación debe esperar hasta que reciba una notificación, si el bloqueo es un problema.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="b3eb0-113">Cuando se llama a esta función, los parámetros deben tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b3eb0-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b3eb0-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*VLOOKUP*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-115">Especifica el identificador que devuelve [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="b3eb0-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-117">Debe ser **SiO \_ NSP \_ Notify \_ Change**.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-119">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-121">Debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="b3eb0-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-123">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-125">Debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="b3eb0-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-127">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3eb0-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span><span class="sxs-lookup"><span data-stu-id="b3eb0-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="b3eb0-129">Especifica **null** o un puntero a una estructura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="b3eb0-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="b3eb0-130">Después de recibir una notificación, llame a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una vez para obtener los resultados.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="b3eb0-131">Para finalizar una búsqueda, llame a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="b3eb0-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="b3eb0-132">Notificaciones de resolución</span><span class="sxs-lookup"><span data-stu-id="b3eb0-132">Resolution Notifications</span></span>

<span data-ttu-id="b3eb0-133">Se puede notificar a un cliente cada vez que se agrega una entrada de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="b3eb0-134">Después, el cliente llama a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para obtener los datos de la resolución.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="b3eb0-135">Si el cliente no usa esta técnica, puede bloquearse una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) hasta que se produzca el tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="b3eb0-136">Notificaciones de lista de nube</span><span class="sxs-lookup"><span data-stu-id="b3eb0-136">Cloud List Notifications</span></span>

<span data-ttu-id="b3eb0-137">Se puede notificar a un cliente en cualquier momento en que se produzca un cambio en un conjunto de nubes.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="b3eb0-138">La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve **WSA \_ E \_ no \_ más** como delimitador de conjunto.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="b3eb0-139">La aplicación cliente debe enumerar las nubes existentes hasta que se devuelva este mensaje y, a continuación, utilizar un esquema de notificación para recuperar los cambios posteriores a medida que se producen.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="b3eb0-140">Una aplicación cliente también puede llamar a **WSALookupServiceNext**, pero la llamada se bloquea hasta que se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="b3eb0-141">La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) devuelve una nube en una estructura **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="b3eb0-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="b3eb0-142">En el miembro **dwOutputFlags** se devuelve una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="b3eb0-143">Value</span><span class="sxs-lookup"><span data-stu-id="b3eb0-143">Value</span></span>               | <span data-ttu-id="b3eb0-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3eb0-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="b3eb0-145">\_se \_ agrega el resultado</span><span class="sxs-lookup"><span data-stu-id="b3eb0-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="b3eb0-146">Se agrega la nube que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="b3eb0-147">el \_ resultado \_ cambia</span><span class="sxs-lookup"><span data-stu-id="b3eb0-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="b3eb0-148">Se cambia la nube que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="b3eb0-149">el resultado \_ se \_ elimina</span><span class="sxs-lookup"><span data-stu-id="b3eb0-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="b3eb0-150">La nube que se devuelve se elimina y no es válida.</span><span class="sxs-lookup"><span data-stu-id="b3eb0-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3eb0-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3eb0-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3eb0-152">PNRP y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="b3eb0-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="b3eb0-153">PNRP y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="b3eb0-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="b3eb0-154">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="b3eb0-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="b3eb0-155">Códigos de error NSP de PNRP</span><span class="sxs-lookup"><span data-stu-id="b3eb0-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="b3eb0-156">**WSANSPIoctl**</span><span class="sxs-lookup"><span data-stu-id="b3eb0-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="b3eb0-157">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="b3eb0-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="b3eb0-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="b3eb0-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="b3eb0-159">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="b3eb0-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



