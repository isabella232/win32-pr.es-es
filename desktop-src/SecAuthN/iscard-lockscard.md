---
description: El método LockSCard notifica el acceso exclusivo a la tarjeta inteligente.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'ISCard:: LockSCard (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278569"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="e7245-103">ISCard:: LockSCard (método)</span><span class="sxs-lookup"><span data-stu-id="e7245-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="e7245-104">\[El método **LockSCard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e7245-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e7245-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7245-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e7245-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e7245-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e7245-107">El método **LockSCard** notifica el acceso exclusivo a la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e7245-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7245-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7245-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="e7245-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7245-109">Parameters</span></span>

<span data-ttu-id="e7245-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7245-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7245-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7245-111">Return value</span></span>

<span data-ttu-id="e7245-112">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="e7245-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e7245-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e7245-113">Return code</span></span>                                                                          | <span data-ttu-id="e7245-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7245-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e7245-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e7245-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7245-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e7245-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7245-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7245-117">Remarks</span></span>

<span data-ttu-id="e7245-118">Además del código de error COM mencionado anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7245-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e7245-119">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e7245-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="e7245-120">Para desbloquear la tarjeta inteligente, llame al método [**ISCard:: UnlockSCard**](iscard-unlockscard.md) .</span><span class="sxs-lookup"><span data-stu-id="e7245-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e7245-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e7245-121">Examples</span></span>

<span data-ttu-id="e7245-122">En el ejemplo siguiente se muestra cómo adquirir acceso exclusivo a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e7245-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="e7245-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7245-123">Requirements</span></span>



| <span data-ttu-id="e7245-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7245-124">Requirement</span></span> | <span data-ttu-id="e7245-125">Value</span><span class="sxs-lookup"><span data-stu-id="e7245-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7245-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7245-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7245-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e7245-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e7245-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7245-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7245-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7245-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7245-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e7245-130">End of client support</span></span><br/>    | <span data-ttu-id="e7245-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7245-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e7245-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e7245-132">End of server support</span></span><br/>    | <span data-ttu-id="e7245-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7245-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e7245-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7245-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7245-135"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7245-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7245-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e7245-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7245-137"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7245-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7245-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7245-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7245-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7245-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7245-140">IID</span><span class="sxs-lookup"><span data-stu-id="e7245-140">IID</span></span><br/>                      | <span data-ttu-id="e7245-141">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e7245-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e7245-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7245-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7245-143">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="e7245-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="e7245-144">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="e7245-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
