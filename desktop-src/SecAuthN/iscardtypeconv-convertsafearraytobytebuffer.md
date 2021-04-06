---
description: Convierte una matriz de bytes definida como SAFEARRAY en un búfer universal de bytes (objeto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'ISCardTypeConv:: ConvertSafeArrayToByteBuffer (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001089"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="b78d5-103">ISCardTypeConv:: ConvertSafeArrayToByteBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="b78d5-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="b78d5-104">\[El método **ConvertSafeArrayToByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b78d5-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b78d5-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b78d5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b78d5-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b78d5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b78d5-107">El método **ConvertSafeArrayToByteBuffer** convierte una matriz de bytes definida como SAFEARRAY en un búfer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="b78d5-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="b78d5-108">El búfer de bytes creado es un flujo asignado a través de un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="b78d5-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="b78d5-109">Para obtener acceso al búfer o administrarlo, utilice los métodos proporcionados por la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b78d5-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="b78d5-110">Una característica única sobre esta implementación de la matriz es que, cuando se llama al método **IStream:: Release** , se liberará la memoria subyacente.</span><span class="sxs-lookup"><span data-stu-id="b78d5-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78d5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b78d5-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="b78d5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b78d5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78d5-113">*pbyArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b78d5-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b78d5-114">Puntero a la matriz SAFEARRAY que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="b78d5-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="b78d5-115">*ppbyBuff* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b78d5-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b78d5-116">Puntero al objeto **IStream** que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="b78d5-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78d5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b78d5-117">Return value</span></span>

<span data-ttu-id="b78d5-118">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="b78d5-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b78d5-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b78d5-119">Return code</span></span>                                                                                   | <span data-ttu-id="b78d5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b78d5-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b78d5-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b78d5-122">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b78d5-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b78d5-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b78d5-124">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="b78d5-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="b78d5-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b78d5-126">Un parámetro de tipo de puntero era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b78d5-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b78d5-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b78d5-128">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b78d5-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b78d5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b78d5-129">Remarks</span></span>

<span data-ttu-id="b78d5-130">La memoria asignada se va a mover.</span><span class="sxs-lookup"><span data-stu-id="b78d5-130">Memory allocated is moveable.</span></span> <span data-ttu-id="b78d5-131">Use el método **IStream:: Release** para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="b78d5-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78d5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b78d5-132">Requirements</span></span>



| <span data-ttu-id="b78d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78d5-133">Requirement</span></span> | <span data-ttu-id="b78d5-134">Value</span><span class="sxs-lookup"><span data-stu-id="b78d5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b78d5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b78d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b78d5-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b78d5-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b78d5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b78d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b78d5-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b78d5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b78d5-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b78d5-139">End of client support</span></span><br/>    | <span data-ttu-id="b78d5-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b78d5-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b78d5-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b78d5-141">End of server support</span></span><br/>    | <span data-ttu-id="b78d5-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b78d5-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b78d5-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b78d5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b78d5-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b78d5-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b78d5-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b78d5-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b78d5-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b78d5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b78d5-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b78d5-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b78d5-149">IID</span><span class="sxs-lookup"><span data-stu-id="b78d5-149">IID</span></span><br/>                      | <span data-ttu-id="b78d5-150">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b78d5-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b78d5-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="b78d5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78d5-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="b78d5-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="b78d5-153">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="b78d5-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
