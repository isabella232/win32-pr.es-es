---
description: La interfaz ISCardDatabase proporciona los métodos para realizar las operaciones de base de datos del administrador de recursos de tarjeta inteligente.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaz ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648203"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="89c95-103">Interfaz ISCardDatabase</span><span class="sxs-lookup"><span data-stu-id="89c95-103">ISCardDatabase interface</span></span>

<span data-ttu-id="89c95-104">\[La interfaz **ISCardDatabase** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="89c95-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="89c95-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89c95-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89c95-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="89c95-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="89c95-107">La interfaz **ISCardDatabase** proporciona los métodos para realizar las operaciones de base [*de datos del administrador de recursos de*](../secgloss/r-gly.md) [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="89c95-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="89c95-108">Entre estas operaciones se incluyen la enumeración de tarjetas inteligentes, [*lectores*](../secgloss/r-gly.md)y grupos de lectores conocidos, además de la recuperación de las interfaces admitidas por una tarjeta inteligente y su [*proveedor de servicios principal*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="89c95-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="89c95-109">El identificador del proveedor de servicios principal es un GUID COM que se puede utilizar para crear instancias y usar los objetos COM para una tarjeta específica.</span><span class="sxs-lookup"><span data-stu-id="89c95-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="89c95-110">En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="89c95-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="89c95-111">En este caso, la interfaz **ISCardDatabase** se usa para enumerar todas las tarjetas inteligentes conocidas.</span><span class="sxs-lookup"><span data-stu-id="89c95-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="89c95-112">**Para enviar una transacción a una tarjeta específica**</span><span class="sxs-lookup"><span data-stu-id="89c95-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="89c95-113">Cree una interfaz **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="89c95-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="89c95-114">Llame a [**ListCards**](iscarddatabase-listcards.md) para recuperar todas las tarjetas inteligentes conocidas basadas en una [*cadena ATR*](../secgloss/a-gly.md) o en sus interfaces admitidas.</span><span class="sxs-lookup"><span data-stu-id="89c95-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="89c95-115">Libere la interfaz **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="89c95-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="89c95-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="89c95-116">Members</span></span>

<span data-ttu-id="89c95-117">La interfaz **ISCardDatabase** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="89c95-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="89c95-118">**ISCardDatabase** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="89c95-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="89c95-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="89c95-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="89c95-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="89c95-120">Methods</span></span>

<span data-ttu-id="89c95-121">La interfaz **ISCardDatabase** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="89c95-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="89c95-122">Método</span><span class="sxs-lookup"><span data-stu-id="89c95-122">Method</span></span>                                                          | <span data-ttu-id="89c95-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="89c95-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89c95-124">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="89c95-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="89c95-125">Recupera el identificador del [*proveedor de servicios principal*](../secgloss/p-gly.md) de una tarjeta inteligente específica.</span><span class="sxs-lookup"><span data-stu-id="89c95-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="89c95-126">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="89c95-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="89c95-127">Recupera los identificadores de interfaz (GUID) de todas las interfaces admitidas por una tarjeta inteligente específica.</span><span class="sxs-lookup"><span data-stu-id="89c95-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="89c95-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="89c95-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="89c95-129">Recupera todos los nombres de tarjetas inteligentes que coinciden con un conjunto específico de identificadores de interfaz (GUID) o una [*cadena ATR*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="89c95-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="89c95-130">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="89c95-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="89c95-131">Recupera los nombres de los [*grupos de lectores*](../secgloss/r-gly.md) de los que el administrador de recursos tiene conocimiento.</span><span class="sxs-lookup"><span data-stu-id="89c95-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="89c95-132">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="89c95-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="89c95-133">Recupere los nombres de los [*lectores*](../secgloss/r-gly.md) de los que el administrador de recursos tiene conocimiento.</span><span class="sxs-lookup"><span data-stu-id="89c95-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="89c95-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c95-134">Requirements</span></span>



| <span data-ttu-id="89c95-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c95-135">Requirement</span></span> | <span data-ttu-id="89c95-136">Value</span><span class="sxs-lookup"><span data-stu-id="89c95-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89c95-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89c95-137">Minimum supported client</span></span><br/> | <span data-ttu-id="89c95-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="89c95-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89c95-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89c95-139">Minimum supported server</span></span><br/> | <span data-ttu-id="89c95-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89c95-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89c95-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="89c95-141">End of client support</span></span><br/>    | <span data-ttu-id="89c95-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89c95-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="89c95-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="89c95-143">End of server support</span></span><br/>    | <span data-ttu-id="89c95-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89c95-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="89c95-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89c95-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c95-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c95-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="89c95-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="89c95-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="89c95-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="89c95-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="89c95-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89c95-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c95-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89c95-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="89c95-151">IID</span><span class="sxs-lookup"><span data-stu-id="89c95-151">IID</span></span><br/>                      | <span data-ttu-id="89c95-152">IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="89c95-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
