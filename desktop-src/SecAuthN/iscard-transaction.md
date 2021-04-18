---
description: Ejecuta una operación de escritura y lectura en el objeto de comando de tarjeta inteligente (unidad de datos de protocolo de aplicación).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard:: Transaction (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652517"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="7290c-103">ISCard:: Transaction (método)</span><span class="sxs-lookup"><span data-stu-id="7290c-103">ISCard::Transaction method</span></span>

<span data-ttu-id="7290c-104">\[El método de **transacción** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7290c-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7290c-105">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7290c-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7290c-106">El método de **transacción** ejecuta una operación de lectura y escritura en el objeto de comando de [*tarjeta inteligente*](../secgloss/s-gly.md) ([*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="7290c-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="7290c-107">La cadena de respuesta de la tarjeta inteligente para la cadena de comando definida en la tarjeta que se envió a la tarjeta inteligente será accesible después de que se devuelva esta función.</span><span class="sxs-lookup"><span data-stu-id="7290c-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="7290c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7290c-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="7290c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7290c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7290c-110">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7290c-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7290c-111">Puntero al objeto de comando de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7290c-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7290c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7290c-112">Return value</span></span>

<span data-ttu-id="7290c-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7290c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7290c-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7290c-114">Return code</span></span>                                                                                   | <span data-ttu-id="7290c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7290c-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7290c-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7290c-117">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7290c-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="7290c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7290c-119">El parámetro *ppCmd* no es válido.</span><span class="sxs-lookup"><span data-stu-id="7290c-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7290c-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7290c-121">Se pasó un puntero no válido en *ppCmd*.</span><span class="sxs-lookup"><span data-stu-id="7290c-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="7290c-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7290c-123">La memoria para satisfacer la solicitud no está disponible.</span><span class="sxs-lookup"><span data-stu-id="7290c-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7290c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7290c-124">Remarks</span></span>

<span data-ttu-id="7290c-125">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7290c-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7290c-126">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7290c-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7290c-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7290c-127">Examples</span></span>

<span data-ttu-id="7290c-128">En el ejemplo siguiente se muestra la ejecución de una operación de escritura y lectura en el objeto de comando de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7290c-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7290c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7290c-129">Requirements</span></span>



| <span data-ttu-id="7290c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7290c-130">Requirement</span></span> | <span data-ttu-id="7290c-131">Value</span><span class="sxs-lookup"><span data-stu-id="7290c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7290c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7290c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7290c-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7290c-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7290c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7290c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7290c-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7290c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7290c-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7290c-136">End of client support</span></span><br/>    | <span data-ttu-id="7290c-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7290c-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7290c-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7290c-138">End of server support</span></span><br/>    | <span data-ttu-id="7290c-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7290c-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7290c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7290c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7290c-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7290c-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7290c-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="7290c-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7290c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7290c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7290c-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7290c-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7290c-146">IID</span><span class="sxs-lookup"><span data-stu-id="7290c-146">IID</span></span><br/>                      | <span data-ttu-id="7290c-147">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7290c-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7290c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="7290c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7290c-149">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="7290c-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="7290c-150">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="7290c-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="7290c-151">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="7290c-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="7290c-152">**obtener \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="7290c-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="7290c-153">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="7290c-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="7290c-154">**obtener \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="7290c-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="7290c-155">**obtener \_ Protocolo**</span><span class="sxs-lookup"><span data-stu-id="7290c-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="7290c-156">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="7290c-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="7290c-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="7290c-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="7290c-158">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="7290c-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="7290c-159">**Volver a adjuntar**</span><span class="sxs-lookup"><span data-stu-id="7290c-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="7290c-160">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="7290c-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
