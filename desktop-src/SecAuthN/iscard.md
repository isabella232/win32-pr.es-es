---
description: Permite abrir y administrar una conexión a una tarjeta inteligente.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaz ISCard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544227"
---
# <a name="iscard-interface"></a><span data-ttu-id="fc3ee-103">Interfaz ISCard</span><span class="sxs-lookup"><span data-stu-id="fc3ee-103">ISCard interface</span></span>

<span data-ttu-id="fc3ee-104">\[La interfaz **ISCard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc3ee-105">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fc3ee-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fc3ee-106">La interfaz **ISCard** permite abrir y administrar una conexión a una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fc3ee-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="fc3ee-107">Cada conexión a una tarjeta requiere una única instancia correspondiente de la interfaz **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="fc3ee-108">El administrador de [*recursos*](../secgloss/r-gly.md) de tarjeta inteligente debe estar disponible cada vez que se cree una instancia de **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="fc3ee-109">Si este servicio no está disponible, se producirá un error en la creación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="fc3ee-110">En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="fc3ee-111">La interfaz **ISCard** se utiliza para conectarse a la tarjeta inteligente, enviar una [*transacción*](../secgloss/t-gly.md)y liberar la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="fc3ee-112">**Para enviar una transacción a una tarjeta específica**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="fc3ee-113">Cree una interfaz **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="fc3ee-114">Asociar a una tarjeta inteligente especificando un [*lector*](../secgloss/r-gly.md) de tarjeta inteligente o usando un identificador válido previamente establecido.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="fc3ee-115">Cree comandos de transacción con las interfaces de tarjeta inteligente [**ISCardCmd**](iscardcmd.md)y [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="fc3ee-116">Use **ISCard** para enviar los comandos de la transacción para su procesamiento por la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="fc3ee-117">Use **ISCard** para liberar la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="fc3ee-118">Libere la interfaz **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="fc3ee-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc3ee-119">Members</span></span>

<span data-ttu-id="fc3ee-120">La interfaz **ISCard** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fc3ee-121">**ISCard** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc3ee-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="fc3ee-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc3ee-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc3ee-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc3ee-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc3ee-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc3ee-124">Methods</span></span>

<span data-ttu-id="fc3ee-125">La interfaz **ISCard** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="fc3ee-126">Método</span><span class="sxs-lookup"><span data-stu-id="fc3ee-126">Method</span></span>                                          | <span data-ttu-id="fc3ee-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc3ee-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc3ee-128">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="fc3ee-129">Asocia un objeto a un identificador de tarjeta inteligente abierto y configurado.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="fc3ee-130">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="fc3ee-131">Abre la tarjeta inteligente en el lector con nombre.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="fc3ee-132">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="fc3ee-133">Cierra la conexión abierta a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="fc3ee-134">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="fc3ee-135">Notifica el acceso exclusivo a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="fc3ee-136">**Volver a adjuntar**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="fc3ee-137">Restablece y reinicializa la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="fc3ee-138">**Transacción**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="fc3ee-139">Ejecuta una operación de escritura y lectura en el objeto de comando de tarjeta inteligente ([*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="fc3ee-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="fc3ee-140">**UnlockScard**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="fc3ee-141">Libera el acceso exclusivo a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="fc3ee-142">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc3ee-142">Properties</span></span>

<span data-ttu-id="fc3ee-143">La interfaz **ISCard** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="fc3ee-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc3ee-144">Property</span></span>                                               | <span data-ttu-id="fc3ee-145">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="fc3ee-145">Access type</span></span>          | <span data-ttu-id="fc3ee-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc3ee-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc3ee-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="fc3ee-148">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc3ee-148">Read-only</span></span><br/> | <span data-ttu-id="fc3ee-149">Recupera la [*cadena ATR*](../secgloss/a-gly.md) de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="fc3ee-150">**CardHandle**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="fc3ee-151">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc3ee-151">Read-only</span></span><br/> | <span data-ttu-id="fc3ee-152">Recupera el identificador de la tarjeta inteligente conectada.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="fc3ee-153">**Context**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="fc3ee-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc3ee-154">Read-only</span></span><br/> | <span data-ttu-id="fc3ee-155">Recupera el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="fc3ee-156">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="fc3ee-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc3ee-157">Read-only</span></span><br/> | <span data-ttu-id="fc3ee-158">Recupera el identificador del protocolo actualmente en uso en la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc3ee-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="fc3ee-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="fc3ee-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="fc3ee-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc3ee-160">Read-only</span></span><br/> | <span data-ttu-id="fc3ee-161">Recupera el [*Estado*](../secgloss/s-gly.md) actual en el que se encuentra la [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3ee-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc3ee-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc3ee-162">Requirements</span></span>



| <span data-ttu-id="fc3ee-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3ee-163">Requirement</span></span> | <span data-ttu-id="fc3ee-164">Value</span><span class="sxs-lookup"><span data-stu-id="fc3ee-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3ee-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc3ee-165">Minimum supported client</span></span><br/> | <span data-ttu-id="fc3ee-166">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fc3ee-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fc3ee-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc3ee-167">Minimum supported server</span></span><br/> | <span data-ttu-id="fc3ee-168">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc3ee-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc3ee-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fc3ee-169">End of client support</span></span><br/>    | <span data-ttu-id="fc3ee-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc3ee-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fc3ee-171">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fc3ee-171">End of server support</span></span><br/>    | <span data-ttu-id="fc3ee-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc3ee-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fc3ee-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc3ee-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc3ee-174"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc3ee-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc3ee-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fc3ee-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc3ee-176"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc3ee-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc3ee-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc3ee-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc3ee-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc3ee-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc3ee-179">IID</span><span class="sxs-lookup"><span data-stu-id="fc3ee-179">IID</span></span><br/>                      | <span data-ttu-id="fc3ee-180">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fc3ee-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
