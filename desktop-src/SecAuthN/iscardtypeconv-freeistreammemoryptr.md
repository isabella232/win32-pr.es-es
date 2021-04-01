---
description: Libera el puntero de bytes que apunta al bloque de memoria HGLOBAL administrado por una interfaz COM IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'ISCardTypeConv:: FreeIStreamMemoryPtr (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814190"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="f52ee-103">ISCardTypeConv:: FreeIStreamMemoryPtr (método)</span><span class="sxs-lookup"><span data-stu-id="f52ee-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="f52ee-104">\[El método **FreeIStreamMemoryPtr** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f52ee-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f52ee-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f52ee-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f52ee-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f52ee-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f52ee-107">El método **FreeIStreamMemoryPtr** libera el puntero de bytes que apunta al bloque de memoria hglobal administrado por una interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="f52ee-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52ee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f52ee-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="f52ee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52ee-110">*pStrm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f52ee-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52ee-111">Puntero a la interfaz **IStream** que administra el bloque de memoria al que apunta *pMem*.</span><span class="sxs-lookup"><span data-stu-id="f52ee-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="f52ee-112">*pMem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f52ee-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52ee-113">Puntero al bloque de memoria administrado por la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="f52ee-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52ee-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52ee-114">Return value</span></span>

<span data-ttu-id="f52ee-115">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="f52ee-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="f52ee-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f52ee-116">Return code</span></span>                                                                                   | <span data-ttu-id="f52ee-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f52ee-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f52ee-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f52ee-119">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f52ee-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f52ee-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f52ee-121">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="f52ee-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="f52ee-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f52ee-123">Un parámetro de tipo de puntero era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f52ee-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f52ee-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f52ee-125">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f52ee-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="f52ee-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f52ee-126">Remarks</span></span>

<span data-ttu-id="f52ee-127">Esta función libera completamente y limpia el puntero de bytes que apunta al bloque de memoria HGLOBAL administrado por la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="f52ee-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="f52ee-128">El puntero de byte se adquiere mediante una llamada a [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span><span class="sxs-lookup"><span data-stu-id="f52ee-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f52ee-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52ee-129">Requirements</span></span>



| <span data-ttu-id="f52ee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52ee-130">Requirement</span></span> | <span data-ttu-id="f52ee-131">Value</span><span class="sxs-lookup"><span data-stu-id="f52ee-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f52ee-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f52ee-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f52ee-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f52ee-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f52ee-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f52ee-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f52ee-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f52ee-136">End of client support</span></span><br/>    | <span data-ttu-id="f52ee-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f52ee-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f52ee-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f52ee-138">End of server support</span></span><br/>    | <span data-ttu-id="f52ee-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f52ee-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f52ee-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52ee-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52ee-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f52ee-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f52ee-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="f52ee-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f52ee-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f52ee-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f52ee-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52ee-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f52ee-146">IID</span><span class="sxs-lookup"><span data-stu-id="f52ee-146">IID</span></span><br/>                      | <span data-ttu-id="f52ee-147">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f52ee-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f52ee-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52ee-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52ee-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="f52ee-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="f52ee-150">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="f52ee-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="f52ee-151">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="f52ee-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
