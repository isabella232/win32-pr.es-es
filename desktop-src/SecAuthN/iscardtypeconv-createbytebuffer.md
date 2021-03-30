---
description: Crea un búfer universal de bytes asignado en un objeto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'ISCardTypeConv:: CreateByteBuffer (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082713"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="e9d3a-103">ISCardTypeConv:: CreateByteBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="e9d3a-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="e9d3a-104">\[El método **CreateByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9d3a-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9d3a-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e9d3a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e9d3a-107">El método **CreateByteBuffer** crea un búfer universal de bytes asignado en un objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="e9d3a-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="e9d3a-108">El búfer de bytes creado es un flujo asignado a través de un bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="e9d3a-109">Para obtener acceso al búfer o administrarlo, utilice los métodos proporcionados por la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="e9d3a-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="e9d3a-110">Una característica única sobre esta implementación de la matriz es que, cuando se llama al método **IStream:: Release** , se liberará la memoria subyacente.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d3a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9d3a-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="e9d3a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9d3a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d3a-113">*dwAllocSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9d3a-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d3a-114">Tamaño en bytes de la memoria que se va a asignar para la matriz.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="e9d3a-115">*ppbyBuff* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e9d3a-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9d3a-116">Puntero al objeto IStream que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d3a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9d3a-117">Return value</span></span>

<span data-ttu-id="e9d3a-118">Los posibles valores devueltos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9d3a-118">The possible return values are the following:</span></span>



| <span data-ttu-id="e9d3a-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e9d3a-119">Return code</span></span>                                                                                   | <span data-ttu-id="e9d3a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9d3a-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9d3a-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9d3a-122">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e9d3a-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e9d3a-124">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="e9d3a-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9d3a-126">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="e9d3a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9d3a-127">Remarks</span></span>

<span data-ttu-id="e9d3a-128">La memoria asignada es movible.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-128">Memory allocated is movable.</span></span> <span data-ttu-id="e9d3a-129">Use el método **IStream:: Release** para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="e9d3a-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="e9d3a-130">Para crear una matriz de bytes de C/C++ típica, llame a [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="e9d3a-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="e9d3a-131">Para crear una matriz SAFEARRAY de Automation de caracteres sin signo (bytes), llame a [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="e9d3a-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d3a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9d3a-132">Requirements</span></span>



| <span data-ttu-id="e9d3a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9d3a-133">Requirement</span></span> | <span data-ttu-id="e9d3a-134">Value</span><span class="sxs-lookup"><span data-stu-id="e9d3a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d3a-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9d3a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d3a-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e9d3a-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9d3a-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9d3a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d3a-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9d3a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9d3a-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e9d3a-139">End of client support</span></span><br/>    | <span data-ttu-id="e9d3a-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9d3a-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e9d3a-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e9d3a-141">End of server support</span></span><br/>    | <span data-ttu-id="e9d3a-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9d3a-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e9d3a-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9d3a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9d3a-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9d3a-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e9d3a-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9d3a-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9d3a-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9d3a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9d3a-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d3a-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9d3a-149">IID</span><span class="sxs-lookup"><span data-stu-id="e9d3a-149">IID</span></span><br/>                      | <span data-ttu-id="e9d3a-150">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e9d3a-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e9d3a-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9d3a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d3a-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="e9d3a-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="e9d3a-153">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e9d3a-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="e9d3a-154">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="e9d3a-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="e9d3a-155">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="e9d3a-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
