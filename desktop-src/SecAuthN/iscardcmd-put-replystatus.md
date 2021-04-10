---
description: Establece una nueva palabra de estado de mensaje APDU de respuesta.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: 'ISCardCmd: método de ut_ReplyStatus de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153836"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="03a98-103">ISCardCmd::p \_ método ReplyStatus UT</span><span class="sxs-lookup"><span data-stu-id="03a98-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="03a98-104">\[El método **Put \_ ReplyStatus** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="03a98-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03a98-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03a98-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="03a98-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="03a98-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="03a98-107">El método **Put \_ ReplyStatus** establece una nueva palabra de estado de mensaje [*APDU de respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="03a98-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a98-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03a98-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="03a98-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03a98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a98-110">*wStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03a98-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03a98-111">Palabra que es el estado.</span><span class="sxs-lookup"><span data-stu-id="03a98-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a98-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03a98-112">Return value</span></span>

<span data-ttu-id="03a98-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="03a98-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="03a98-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="03a98-114">Return code</span></span>                                                                                   | <span data-ttu-id="03a98-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="03a98-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="03a98-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="03a98-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="03a98-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="03a98-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="03a98-119">El parámetro *wStatus* no es válido.</span><span class="sxs-lookup"><span data-stu-id="03a98-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="03a98-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="03a98-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="03a98-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="03a98-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03a98-122">Remarks</span></span>

<span data-ttu-id="03a98-123">Para obtener la palabra de estado de mensaje de APDU de respuesta, llame a [**Get \_ ReplyStatus**](iscardcmd-get-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="03a98-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="03a98-124">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="03a98-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="03a98-125">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03a98-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="03a98-126">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="03a98-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="03a98-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="03a98-127">Examples</span></span>

<span data-ttu-id="03a98-128">En el ejemplo siguiente se muestra cómo establecer una nueva palabra de estado de mensaje [*APDU de respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="03a98-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="03a98-129">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="03a98-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="03a98-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03a98-130">Requirements</span></span>



| <span data-ttu-id="03a98-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a98-131">Requirement</span></span> | <span data-ttu-id="03a98-132">Value</span><span class="sxs-lookup"><span data-stu-id="03a98-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03a98-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a98-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03a98-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="03a98-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03a98-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a98-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03a98-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="03a98-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03a98-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="03a98-137">End of client support</span></span><br/>    | <span data-ttu-id="03a98-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="03a98-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="03a98-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="03a98-139">End of server support</span></span><br/>    | <span data-ttu-id="03a98-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03a98-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="03a98-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03a98-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a98-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="03a98-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="03a98-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="03a98-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03a98-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03a98-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a98-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="03a98-147">IID</span><span class="sxs-lookup"><span data-stu-id="03a98-147">IID</span></span><br/>                      | <span data-ttu-id="03a98-148">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="03a98-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="03a98-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="03a98-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a98-150">**obtener \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="03a98-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="03a98-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="03a98-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
