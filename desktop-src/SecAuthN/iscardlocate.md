---
description: La interfaz ISCardLocate proporciona servicios para buscar una tarjeta inteligente por su nombre.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interfaz ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648458"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="7844e-103">Interfaz ISCardLocate</span><span class="sxs-lookup"><span data-stu-id="7844e-103">ISCardLocate interface</span></span>

<span data-ttu-id="7844e-104">\[La interfaz **ISCardLocate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7844e-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7844e-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7844e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7844e-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7844e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7844e-107">La interfaz **ISCardLocate** proporciona servicios para buscar una [*tarjeta inteligente*](../secgloss/s-gly.md) por su nombre.</span><span class="sxs-lookup"><span data-stu-id="7844e-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="7844e-108">Esta interfaz puede mostrar la interfaz de [*usuario*](../secgloss/u-gly.md) de la tarjeta inteligente si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7844e-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="7844e-109">En el escenario siguiente se muestra un uso típico de la interfaz **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="7844e-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="7844e-110">La interfaz **ISCardLocate** se utiliza para compilar una [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="7844e-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="7844e-111">**Para buscar una tarjeta específica con su nombre**</span><span class="sxs-lookup"><span data-stu-id="7844e-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="7844e-112">Cree una interfaz **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="7844e-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="7844e-113">Llame a [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para buscar un nombre de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7844e-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="7844e-114">Llame a [**FindCard**](iscardlocate-findcard.md) para buscar la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7844e-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="7844e-115">Interpretará los resultados.</span><span class="sxs-lookup"><span data-stu-id="7844e-115">Interpret the results.</span></span>
5.  <span data-ttu-id="7844e-116">Libere la interfaz **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="7844e-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="7844e-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="7844e-117">Members</span></span>

<span data-ttu-id="7844e-118">La interfaz **ISCardLocate** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7844e-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7844e-119">**ISCardLocate** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7844e-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="7844e-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="7844e-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7844e-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="7844e-121">Methods</span></span>

<span data-ttu-id="7844e-122">La interfaz **ISCardLocate** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7844e-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="7844e-123">Método</span><span class="sxs-lookup"><span data-stu-id="7844e-123">Method</span></span>                                                                  | <span data-ttu-id="7844e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7844e-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="7844e-125">**ConfigureCardGuidSearch**</span><span class="sxs-lookup"><span data-stu-id="7844e-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="7844e-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7844e-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="7844e-127">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="7844e-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="7844e-128">Especifica el nombre de la tarjeta que se va a usar en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7844e-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="7844e-129">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="7844e-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="7844e-130">Busca la tarjeta inteligente y abre una conexión válida con ella.</span><span class="sxs-lookup"><span data-stu-id="7844e-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7844e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7844e-131">Requirements</span></span>



| <span data-ttu-id="7844e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7844e-132">Requirement</span></span> | <span data-ttu-id="7844e-133">Value</span><span class="sxs-lookup"><span data-stu-id="7844e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7844e-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7844e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7844e-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7844e-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7844e-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7844e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7844e-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7844e-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7844e-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7844e-138">End of client support</span></span><br/>    | <span data-ttu-id="7844e-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7844e-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7844e-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7844e-140">End of server support</span></span><br/>    | <span data-ttu-id="7844e-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7844e-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7844e-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7844e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7844e-143"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7844e-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7844e-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7844e-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="7844e-145"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7844e-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7844e-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7844e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7844e-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7844e-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7844e-148">IID</span><span class="sxs-lookup"><span data-stu-id="7844e-148">IID</span></span><br/>                      | <span data-ttu-id="7844e-149">IID \_ ISCardLocate se define como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7844e-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
