---
description: Convierte un búfer universal de bytes (objeto IStream) en un SAFEARRAY de char sin signo (byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'ISCardTypeConv:: ConvertByteBufferToSafeArray (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814734"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a><span data-ttu-id="e538f-103">ISCardTypeConv:: ConvertByteBufferToSafeArray (método)</span><span class="sxs-lookup"><span data-stu-id="e538f-103">ISCardTypeConv::ConvertByteBufferToSafeArray method</span></span>

<span data-ttu-id="e538f-104">\[El método **ConvertByteBufferToSafeArray** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e538f-104">\[The **ConvertByteBufferToSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e538f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e538f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e538f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e538f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e538f-107">El método **ConvertByteBufferToSafeArray** convierte un búfer universal de bytes (objeto **IStream** ) en un SafeArray de char sin signo (byte).</span><span class="sxs-lookup"><span data-stu-id="e538f-107">The **ConvertByteBufferToSafeArray** method converts a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span>

## <a name="syntax"></a><span data-ttu-id="e538f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e538f-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="e538f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e538f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e538f-110">*pbyBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e538f-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e538f-111">Puntero al objeto **IStream** que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e538f-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="e538f-112">*ppbyArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e538f-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e538f-113">Puntero a la matriz SAFEARRAY que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="e538f-113">Pointer to the SAFEARRAY to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e538f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e538f-114">Return value</span></span>

<span data-ttu-id="e538f-115">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="e538f-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="e538f-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e538f-116">Return code</span></span>                                                                                   | <span data-ttu-id="e538f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e538f-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e538f-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e538f-119">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e538f-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e538f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e538f-121">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="e538f-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="e538f-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e538f-123">Un parámetro de tipo de puntero era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="e538f-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e538f-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e538f-125">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e538f-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="e538f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e538f-126">Requirements</span></span>



| <span data-ttu-id="e538f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e538f-127">Requirement</span></span> | <span data-ttu-id="e538f-128">Value</span><span class="sxs-lookup"><span data-stu-id="e538f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e538f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e538f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e538f-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e538f-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e538f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e538f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e538f-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e538f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e538f-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e538f-133">End of client support</span></span><br/>    | <span data-ttu-id="e538f-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e538f-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e538f-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e538f-135">End of server support</span></span><br/>    | <span data-ttu-id="e538f-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e538f-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e538f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e538f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e538f-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e538f-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e538f-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="e538f-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e538f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e538f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e538f-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e538f-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e538f-143">IID</span><span class="sxs-lookup"><span data-stu-id="e538f-143">IID</span></span><br/>                      | <span data-ttu-id="e538f-144">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e538f-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e538f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e538f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e538f-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="e538f-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="e538f-147">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e538f-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
