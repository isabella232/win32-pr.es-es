---
description: Adquiere un puntero de byte al bloque de memoria HGLOBAL administrado por la interfaz COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv:: GetAtIStreamMemory (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808677"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="d6f83-103">ISCardTypeConv:: GetAtIStreamMemory (método)</span><span class="sxs-lookup"><span data-stu-id="d6f83-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="d6f83-104">\[El método **GetAtIStreamMemory** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d6f83-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6f83-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d6f83-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d6f83-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d6f83-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d6f83-107">El método **GetAtIStreamMemory** adquiere un puntero de byte al bloque de memoria hglobal administrado por la interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="d6f83-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="d6f83-108">Se trata de una manera de obtener la memoria en la **IStream** sin tener que obtener el valor sizeof para el bloque de memoria en bytes y leer los bytes en una matriz de bytes temporal mediante la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="d6f83-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f83-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6f83-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="d6f83-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6f83-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f83-111">*pStrm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6f83-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f83-112">Puntero a la interfaz com **IStream** que administra el bloque de memoria hglobal.</span><span class="sxs-lookup"><span data-stu-id="d6f83-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="d6f83-113">*ppMem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d6f83-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f83-114">Puntero al primer byte del bloque de memoria HGLOBAL si se realiza correctamente; en caso contrario, **null** si se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="d6f83-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f83-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6f83-115">Return value</span></span>

<span data-ttu-id="d6f83-116">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d6f83-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d6f83-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d6f83-117">Return code</span></span>                                                                                   | <span data-ttu-id="d6f83-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6f83-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6f83-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d6f83-120">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6f83-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d6f83-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d6f83-122">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="d6f83-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="d6f83-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d6f83-124">Un parámetro de tipo de puntero era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="d6f83-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d6f83-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d6f83-126">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6f83-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d6f83-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6f83-127">Remarks</span></span>

<span data-ttu-id="d6f83-128">El recuento de referencias de **IStream** se incrementará para cada puntero *ppMem* adquirido.</span><span class="sxs-lookup"><span data-stu-id="d6f83-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f83-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f83-129">Requirements</span></span>



| <span data-ttu-id="d6f83-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f83-130">Requirement</span></span> | <span data-ttu-id="d6f83-131">Value</span><span class="sxs-lookup"><span data-stu-id="d6f83-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f83-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6f83-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f83-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d6f83-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d6f83-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6f83-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f83-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6f83-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6f83-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d6f83-136">End of client support</span></span><br/>    | <span data-ttu-id="d6f83-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6f83-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d6f83-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d6f83-138">End of server support</span></span><br/>    | <span data-ttu-id="d6f83-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6f83-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d6f83-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6f83-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f83-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6f83-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d6f83-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6f83-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6f83-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6f83-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f83-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f83-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6f83-146">IID</span><span class="sxs-lookup"><span data-stu-id="d6f83-146">IID</span></span><br/>                      | <span data-ttu-id="d6f83-147">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d6f83-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d6f83-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6f83-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f83-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="d6f83-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="d6f83-150">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="d6f83-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
