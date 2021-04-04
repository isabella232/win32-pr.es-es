---
description: Libera el acceso exclusivo a la tarjeta inteligente.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'ISCard:: UnlockSCard (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811791"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="2b7f6-103">ISCard:: UnlockSCard (método)</span><span class="sxs-lookup"><span data-stu-id="2b7f6-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="2b7f6-104">\[El método **UnlockScard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b7f6-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b7f6-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2b7f6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2b7f6-107">El método **UnlockScard** libera el acceso exclusivo a la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b7f6-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7f6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b7f6-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="2b7f6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b7f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b7f6-110">*Disposición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b7f6-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b7f6-111">Indica qué se debe hacer con la tarjeta en el [*lector*](../secgloss/r-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="2b7f6-112">Value</span><span class="sxs-lookup"><span data-stu-id="2b7f6-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="2b7f6-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2b7f6-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="2b7f6-114"><dt>**OMITI**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="2b7f6-115">Deja la tarjeta inteligente en el [*Estado*](../secgloss/s-gly.md)actual.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="2b7f6-116"><dt>**DETERMINADO**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="2b7f6-117">Restablece la tarjeta inteligente a algún estado conocido.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="2b7f6-118"><dt>**No energía**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="2b7f6-119">Quita la energía de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="2b7f6-120"><dt>**EXPULSAR**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="2b7f6-121">Expulsa la tarjeta inteligente si el lector tiene capacidades de expulsión.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b7f6-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b7f6-122">Return value</span></span>

<span data-ttu-id="2b7f6-123">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2b7f6-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2b7f6-124">Return code</span></span>                                                                                  | <span data-ttu-id="2b7f6-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b7f6-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="2b7f6-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2b7f6-127">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="2b7f6-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2b7f6-129">El parámetro de *disposición* no es válido</span><span class="sxs-lookup"><span data-stu-id="2b7f6-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b7f6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b7f6-130">Remarks</span></span>

<span data-ttu-id="2b7f6-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2b7f6-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2b7f6-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2b7f6-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b7f6-133">Examples</span></span>

<span data-ttu-id="2b7f6-134">En el ejemplo siguiente se muestra cómo liberar el acceso exclusivo a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="2b7f6-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2b7f6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7f6-135">Requirements</span></span>



| <span data-ttu-id="2b7f6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7f6-136">Requirement</span></span> | <span data-ttu-id="2b7f6-137">Value</span><span class="sxs-lookup"><span data-stu-id="2b7f6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7f6-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7f6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7f6-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2b7f6-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2b7f6-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b7f6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7f6-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b7f6-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b7f6-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2b7f6-142">End of client support</span></span><br/>    | <span data-ttu-id="2b7f6-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b7f6-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2b7f6-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2b7f6-144">End of server support</span></span><br/>    | <span data-ttu-id="2b7f6-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b7f6-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2b7f6-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b7f6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b7f6-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b7f6-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b7f6-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b7f6-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b7f6-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b7f6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b7f6-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b7f6-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b7f6-152">IID</span><span class="sxs-lookup"><span data-stu-id="2b7f6-152">IID</span></span><br/>                      | <span data-ttu-id="2b7f6-153">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2b7f6-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2b7f6-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b7f6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7f6-155">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="2b7f6-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2b7f6-156">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="2b7f6-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
