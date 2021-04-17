---
description: El método GetResponse crea un comando de unidad de datos de protocolo de aplicación (APDU) que transmite Comandos APDU (o parte de un comando APDU) que, de lo contrario, los protocolos disponibles no podrían transmitir.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'ISCardISO7816:: GetResponse (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652879"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="3edd5-103">ISCardISO7816:: GetResponse (método)</span><span class="sxs-lookup"><span data-stu-id="3edd5-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="3edd5-104">\[El método **GetResponse** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3edd5-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3edd5-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3edd5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3edd5-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3edd5-107">El método **GetResponse** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que transmite Comandos APDU (o parte de un comando APDU) que, de lo contrario, los protocolos disponibles no podrían transmitir.</span><span class="sxs-lookup"><span data-stu-id="3edd5-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="3edd5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3edd5-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="3edd5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3edd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3edd5-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd5-111">Según la norma ISO 7816-4, P1 debe ser cero (RFU).</span><span class="sxs-lookup"><span data-stu-id="3edd5-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="3edd5-112">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd5-113">Según la ISO 7816-4, P2 debe ser cero (RFU).</span><span class="sxs-lookup"><span data-stu-id="3edd5-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="3edd5-114">*lDataLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd5-115">Longitud de los datos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="3edd5-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="3edd5-116">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd5-117">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="3edd5-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="3edd5-118">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="3edd5-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="3edd5-119">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="3edd5-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3edd5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3edd5-120">Return value</span></span>

<span data-ttu-id="3edd5-121">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3edd5-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3edd5-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3edd5-122">Return code</span></span>                                                                                   | <span data-ttu-id="3edd5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3edd5-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3edd5-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3edd5-125">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3edd5-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3edd5-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3edd5-127">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="3edd5-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3edd5-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3edd5-129">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="3edd5-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3edd5-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3edd5-131">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="3edd5-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3edd5-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3edd5-132">Remarks</span></span>

<span data-ttu-id="3edd5-133">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="3edd5-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="3edd5-134">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3edd5-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3edd5-135">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3edd5-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3edd5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3edd5-136">Requirements</span></span>



| <span data-ttu-id="3edd5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3edd5-137">Requirement</span></span> | <span data-ttu-id="3edd5-138">Value</span><span class="sxs-lookup"><span data-stu-id="3edd5-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3edd5-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3edd5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3edd5-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3edd5-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3edd5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3edd5-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3edd5-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3edd5-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3edd5-143">End of client support</span></span><br/>    | <span data-ttu-id="3edd5-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3edd5-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3edd5-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3edd5-145">End of server support</span></span><br/>    | <span data-ttu-id="3edd5-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3edd5-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3edd5-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3edd5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3edd5-148"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3edd5-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3edd5-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="3edd5-150"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3edd5-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3edd5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3edd5-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3edd5-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3edd5-153">IID</span><span class="sxs-lookup"><span data-stu-id="3edd5-153">IID</span></span><br/>                      | <span data-ttu-id="3edd5-154">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3edd5-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3edd5-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="3edd5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3edd5-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="3edd5-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
