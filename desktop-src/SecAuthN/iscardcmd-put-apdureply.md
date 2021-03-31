---
description: Establece una nueva APDU de respuesta.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'ISCardCmd: método de ut_ApduReply de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907983"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="c5e6b-103">ISCardCmd::p \_ método ApduReply UT</span><span class="sxs-lookup"><span data-stu-id="c5e6b-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="c5e6b-104">\[El método **Put \_ ApduReply** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5e6b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c5e6b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c5e6b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c5e6b-107">El método **Put \_ ApduReply** establece una nueva [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6b-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5e6b-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="c5e6b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5e6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e6b-110">*pReplyApdu* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5e6b-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e6b-111">Puntero al búfer de bytes (asignado a través de un objeto **IStream** ) que contiene el mensaje APDU de reproducción en la devolución.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e6b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5e6b-112">Return value</span></span>

<span data-ttu-id="c5e6b-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c5e6b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c5e6b-114">Return code</span></span>                                                                                   | <span data-ttu-id="c5e6b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5e6b-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c5e6b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c5e6b-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="c5e6b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c5e6b-119">El parámetro *pReplyApdu* no es válido.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c5e6b-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c5e6b-121">Se pasó un puntero no válido en *pReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="c5e6b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c5e6b-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="c5e6b-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c5e6b-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5e6b-124">Remarks</span></span>

<span data-ttu-id="c5e6b-125">Para obtener una APDU de respuesta existente, llame a [**Get \_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6b-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="c5e6b-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6b-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c5e6b-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5e6b-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c5e6b-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5e6b-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c5e6b-129">Examples</span></span>

<span data-ttu-id="c5e6b-130">En el ejemplo siguiente se muestra cómo establecer una nueva [*APDU de respuesta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6b-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="c5e6b-131">En el ejemplo se da por supuesto que pIByteReply es un puntero válido a una instancia de [**IByteBuffer**](ibytebuffer.md)y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e6b-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c5e6b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e6b-132">Requirements</span></span>



| <span data-ttu-id="c5e6b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e6b-133">Requirement</span></span> | <span data-ttu-id="c5e6b-134">Value</span><span class="sxs-lookup"><span data-stu-id="c5e6b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e6b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e6b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e6b-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e6b-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c5e6b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5e6b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e6b-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e6b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5e6b-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c5e6b-139">End of client support</span></span><br/>    | <span data-ttu-id="c5e6b-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5e6b-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c5e6b-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c5e6b-141">End of server support</span></span><br/>    | <span data-ttu-id="c5e6b-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5e6b-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c5e6b-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5e6b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e6b-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5e6b-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5e6b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5e6b-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5e6b-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5e6b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5e6b-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5e6b-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5e6b-149">IID</span><span class="sxs-lookup"><span data-stu-id="c5e6b-149">IID</span></span><br/>                      | <span data-ttu-id="c5e6b-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c5e6b-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c5e6b-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e6b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e6b-152">**obtener \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="c5e6b-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="c5e6b-153">**obtener \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="c5e6b-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="c5e6b-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="c5e6b-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
