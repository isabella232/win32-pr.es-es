---
description: Recupera el APDU de respuesta, colocándolo en un búfer de bytes específico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Método ISCardCmd:: get_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083434"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="15601-103">ISCardCmd:: get \_ ApduReply (método)</span><span class="sxs-lookup"><span data-stu-id="15601-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="15601-104">\[El método **Get \_ ApduReply** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="15601-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="15601-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="15601-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15601-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="15601-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="15601-107">El método **Get \_ ApduReply** recupera el [*APDU de respuesta*](../secgloss/r-gly.md)y lo coloca en un búfer de bytes específico.</span><span class="sxs-lookup"><span data-stu-id="15601-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="15601-108">La respuesta puede ser **null** si no se ha realizado ninguna [*transacción*](../secgloss/t-gly.md) en el comando APDU.</span><span class="sxs-lookup"><span data-stu-id="15601-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="15601-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15601-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="15601-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15601-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15601-111">*ppReplyApdu* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="15601-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15601-112">Puntero al búfer de bytes (asignado a través de un objeto **IStream** ) que contiene el mensaje de respuesta APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="15601-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15601-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15601-113">Return value</span></span>

<span data-ttu-id="15601-114">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="15601-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="15601-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="15601-115">Return code</span></span>                                                                                   | <span data-ttu-id="15601-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="15601-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="15601-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="15601-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="15601-118">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="15601-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="15601-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="15601-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="15601-120">El parámetro *ppReplyApdu* no es válido.</span><span class="sxs-lookup"><span data-stu-id="15601-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="15601-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="15601-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="15601-122">Se pasó un puntero no válido en *ppReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="15601-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="15601-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="15601-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="15601-124">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="15601-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="15601-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15601-125">Remarks</span></span>

<span data-ttu-id="15601-126">Para determinar la longitud de la respuesta APDU, llame a [**Get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="15601-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="15601-127">Para establecer una nueva APDU de respuesta, llame a [**Put \_ ApduReply**](iscardcmd-put-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="15601-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="15601-128">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="15601-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="15601-129">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15601-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="15601-130">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="15601-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="15601-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="15601-131">Examples</span></span>

<span data-ttu-id="15601-132">En el ejemplo siguiente se muestra cómo recuperar los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15601-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="15601-133">En el ejemplo se da por supuesto que lLe es una variable de tipo **Long** cuyo valor fue establecido por una llamada anterior al método [**ISCardCmd:: get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , que pIByteReply es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="15601-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="15601-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15601-134">Requirements</span></span>



| <span data-ttu-id="15601-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="15601-135">Requirement</span></span> | <span data-ttu-id="15601-136">Value</span><span class="sxs-lookup"><span data-stu-id="15601-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15601-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15601-137">Minimum supported client</span></span><br/> | <span data-ttu-id="15601-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="15601-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="15601-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15601-139">Minimum supported server</span></span><br/> | <span data-ttu-id="15601-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15601-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15601-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="15601-141">End of client support</span></span><br/>    | <span data-ttu-id="15601-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="15601-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="15601-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="15601-143">End of server support</span></span><br/>    | <span data-ttu-id="15601-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15601-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="15601-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15601-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="15601-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="15601-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="15601-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="15601-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="15601-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15601-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15601-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15601-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15601-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15601-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15601-151">IID</span><span class="sxs-lookup"><span data-stu-id="15601-151">IID</span></span><br/>                      | <span data-ttu-id="15601-152">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="15601-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="15601-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="15601-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15601-154">**obtener \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="15601-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="15601-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="15601-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="15601-156">**Put \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="15601-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
