---
description: La interfaz IByteBuffer se proporciona para leer, escribir y administrar objetos de secuencia. Básicamente, este objeto es un contenedor para el objeto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interfaz IByteBuffer (Scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002756"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="5e48e-104">Interfaz IByteBuffer</span><span class="sxs-lookup"><span data-stu-id="5e48e-104">IByteBuffer interface</span></span>

<span data-ttu-id="5e48e-105">\[La interfaz **IByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5e48e-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5e48e-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e48e-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5e48e-107">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5e48e-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="5e48e-108">La interfaz **IByteBuffer** se proporciona para leer, escribir y administrar objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e48e-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="5e48e-109">Básicamente, este objeto es un contenedor para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5e48e-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="5e48e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e48e-110">Members</span></span>

<span data-ttu-id="5e48e-111">La interfaz **IByteBuffer** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5e48e-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5e48e-112">**IByteBuffer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e48e-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="5e48e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e48e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e48e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e48e-114">Methods</span></span>

<span data-ttu-id="5e48e-115">La interfaz **IByteBuffer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5e48e-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="5e48e-116">Método</span><span class="sxs-lookup"><span data-stu-id="5e48e-116">Method</span></span>                                           | <span data-ttu-id="5e48e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e48e-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e48e-118">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="5e48e-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="5e48e-119">Clona un objeto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="5e48e-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="5e48e-120">**Promete**</span><span class="sxs-lookup"><span data-stu-id="5e48e-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="5e48e-121">Confirma una [*transacción*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="5e48e-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="5e48e-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="5e48e-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="5e48e-123">Copia bytes en otro objeto.</span><span class="sxs-lookup"><span data-stu-id="5e48e-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="5e48e-124">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="5e48e-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="5e48e-125">Inicializa el objeto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="5e48e-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="5e48e-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="5e48e-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="5e48e-127">Restringe el acceso a un intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="5e48e-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="5e48e-128">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="5e48e-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="5e48e-129">Lee bytes en la memoria.</span><span class="sxs-lookup"><span data-stu-id="5e48e-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="5e48e-130">**Revertir**</span><span class="sxs-lookup"><span data-stu-id="5e48e-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="5e48e-131">Descarta los cambios desde la última llamada de [**confirmación**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="5e48e-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="5e48e-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="5e48e-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="5e48e-133">Cambia el puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5e48e-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="5e48e-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="5e48e-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="5e48e-135">Cambia el tamaño del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e48e-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="5e48e-136">**Estadística**</span><span class="sxs-lookup"><span data-stu-id="5e48e-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="5e48e-137">Recupera información estadística sobre un flujo.</span><span class="sxs-lookup"><span data-stu-id="5e48e-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="5e48e-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="5e48e-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="5e48e-139">Quita la restricción de acceso establecida previamente por [**LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="5e48e-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="5e48e-140">**Escritura**</span><span class="sxs-lookup"><span data-stu-id="5e48e-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="5e48e-141">Escribe bytes en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e48e-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="5e48e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e48e-142">Requirements</span></span>



| <span data-ttu-id="5e48e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e48e-143">Requirement</span></span> | <span data-ttu-id="5e48e-144">Value</span><span class="sxs-lookup"><span data-stu-id="5e48e-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e48e-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e48e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5e48e-146">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5e48e-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5e48e-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e48e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5e48e-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e48e-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e48e-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5e48e-149">End of client support</span></span><br/>    | <span data-ttu-id="5e48e-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e48e-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5e48e-151">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5e48e-151">End of server support</span></span><br/>    | <span data-ttu-id="5e48e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e48e-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5e48e-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e48e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e48e-154"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e48e-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e48e-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5e48e-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e48e-156"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e48e-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e48e-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e48e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e48e-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e48e-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e48e-159">IID</span><span class="sxs-lookup"><span data-stu-id="5e48e-159">IID</span></span><br/>                      | <span data-ttu-id="5e48e-160">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="5e48e-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

