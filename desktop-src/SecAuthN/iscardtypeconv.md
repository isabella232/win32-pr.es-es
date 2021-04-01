---
description: Proporciona los métodos necesarios para admitir los usuarios de las otras interfaces COM de tarjeta inteligente.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interfaz ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909657"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="411b2-103">Interfaz ISCardTypeConv</span><span class="sxs-lookup"><span data-stu-id="411b2-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="411b2-104">\[La interfaz **ISCardTypeConv** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="411b2-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="411b2-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="411b2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="411b2-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="411b2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="411b2-107">La interfaz **ISCardTypeConv** proporciona los métodos necesarios para admitir los usuarios de las otras interfaces com de [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="411b2-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="411b2-108">Esta interfaz se proporciona solo para la compatibilidad con versiones anteriores y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="411b2-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="411b2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="411b2-109">Members</span></span>

<span data-ttu-id="411b2-110">La interfaz **ISCardTypeConv** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="411b2-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="411b2-111">**ISCardTypeConv** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="411b2-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="411b2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="411b2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="411b2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="411b2-113">Methods</span></span>

<span data-ttu-id="411b2-114">La interfaz **ISCardTypeConv** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="411b2-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="411b2-115">Método</span><span class="sxs-lookup"><span data-stu-id="411b2-115">Method</span></span>                                                                              | <span data-ttu-id="411b2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="411b2-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="411b2-117">**ConvertByteArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="411b2-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="411b2-118">Convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="411b2-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="411b2-119">**ConvertByteBufferToByteArray**</span><span class="sxs-lookup"><span data-stu-id="411b2-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="411b2-120">Convierte una matriz de bytes asignada en un búfer universal de bytes (objeto **IStream** ) en una matriz de bytes de C/C++ típica.</span><span class="sxs-lookup"><span data-stu-id="411b2-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="411b2-121">**ConvertByteBufferToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="411b2-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="411b2-122">Convierte una matriz de bytes asignada en un búfer universal de bytes (objeto **IStream** ) en una SafeArray de char sin signo (byte).</span><span class="sxs-lookup"><span data-stu-id="411b2-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="411b2-123">**ConvertSafeArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="411b2-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="411b2-124">Convierte una matriz de bytes definida como SAFEARRAY en un búfer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="411b2-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="411b2-125">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="411b2-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="411b2-126">Crea una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="411b2-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="411b2-127">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="411b2-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="411b2-128">Crea un búfer universal de bytes asignado en un objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="411b2-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="411b2-129">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="411b2-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="411b2-130">Crea una matriz SAFEARRAY de automatización de caracteres sin signo (bytes).</span><span class="sxs-lookup"><span data-stu-id="411b2-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="411b2-131">**FreeIStreamMemoryPtr**</span><span class="sxs-lookup"><span data-stu-id="411b2-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="411b2-132">Libera un puntero de memoria para el bloque de memoria HGLOBAL administrado por una interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="411b2-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="411b2-133">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="411b2-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="411b2-134">Adquiere un puntero de byte al bloque de memoria HGLOBAL administrado por la interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="411b2-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="411b2-135">**SizeOfIStream**</span><span class="sxs-lookup"><span data-stu-id="411b2-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="411b2-136">Determina el tamaño (número de bytes) de una interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="411b2-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="411b2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="411b2-137">Requirements</span></span>



| <span data-ttu-id="411b2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="411b2-138">Requirement</span></span> | <span data-ttu-id="411b2-139">Value</span><span class="sxs-lookup"><span data-stu-id="411b2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="411b2-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="411b2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="411b2-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="411b2-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="411b2-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="411b2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="411b2-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="411b2-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="411b2-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="411b2-144">End of client support</span></span><br/>    | <span data-ttu-id="411b2-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="411b2-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="411b2-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="411b2-146">End of server support</span></span><br/>    | <span data-ttu-id="411b2-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="411b2-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="411b2-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="411b2-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="411b2-149"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="411b2-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="411b2-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="411b2-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="411b2-151"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="411b2-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="411b2-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="411b2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411b2-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="411b2-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="411b2-154">IID</span><span class="sxs-lookup"><span data-stu-id="411b2-154">IID</span></span><br/>                      | <span data-ttu-id="411b2-155">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="411b2-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
