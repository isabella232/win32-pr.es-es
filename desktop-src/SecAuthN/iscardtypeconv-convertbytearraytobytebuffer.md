---
description: Convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv:: ConvertByteArrayToByteBuffer (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912457"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="0783f-103">ISCardTypeConv:: ConvertByteArrayToByteBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="0783f-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="0783f-104">\[El método **ConvertByteArrayToByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0783f-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0783f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0783f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0783f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0783f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0783f-107">El método **ConvertByteArrayToByteBuffer** convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="0783f-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="0783f-108">El búfer de bytes creado es un flujo asignado a través de un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="0783f-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="0783f-109">Para obtener acceso al búfer o administrarlo, utilice los métodos proporcionados por la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0783f-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="0783f-110">Una característica única sobre esta implementación de la matriz es que, cuando se llama al método **IStream:: Release** , se liberará la memoria subyacente.</span><span class="sxs-lookup"><span data-stu-id="0783f-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="0783f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0783f-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0783f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0783f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0783f-113">*pbyArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0783f-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0783f-114">Puntero a la matriz de bytes que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="0783f-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="0783f-115">*dwArraySize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0783f-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0783f-116">Tamaño de la matriz de bytes que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="0783f-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="0783f-117">*ppbyBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0783f-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0783f-118">Puntero al objeto **IStream** que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="0783f-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0783f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0783f-119">Return value</span></span>

<span data-ttu-id="0783f-120">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="0783f-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="0783f-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0783f-121">Return code</span></span>                                                                                   | <span data-ttu-id="0783f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0783f-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0783f-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0783f-124">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0783f-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0783f-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0783f-126">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="0783f-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="0783f-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0783f-128">Un parámetro de tipo de puntero era incorrecto.</span><span class="sxs-lookup"><span data-stu-id="0783f-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0783f-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0783f-130">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0783f-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="0783f-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0783f-131">Remarks</span></span>

<span data-ttu-id="0783f-132">La memoria asignada es movible.</span><span class="sxs-lookup"><span data-stu-id="0783f-132">Memory allocated is movable.</span></span> <span data-ttu-id="0783f-133">Use el método **IStream:: Release** para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="0783f-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="0783f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0783f-134">Requirements</span></span>



| <span data-ttu-id="0783f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0783f-135">Requirement</span></span> | <span data-ttu-id="0783f-136">Value</span><span class="sxs-lookup"><span data-stu-id="0783f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0783f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0783f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0783f-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0783f-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0783f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0783f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0783f-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0783f-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0783f-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0783f-141">End of client support</span></span><br/>    | <span data-ttu-id="0783f-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0783f-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0783f-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0783f-143">End of server support</span></span><br/>    | <span data-ttu-id="0783f-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0783f-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0783f-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0783f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0783f-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0783f-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0783f-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="0783f-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0783f-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0783f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0783f-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0783f-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0783f-151">IID</span><span class="sxs-lookup"><span data-stu-id="0783f-151">IID</span></span><br/>                      | <span data-ttu-id="0783f-152">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0783f-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0783f-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0783f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0783f-154">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="0783f-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="0783f-155">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="0783f-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
