---
description: Cierra la conexión abierta a la tarjeta inteligente.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: ISCard::D método Etach (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649180"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="626a3-103">ISCard::D método Etach</span><span class="sxs-lookup"><span data-stu-id="626a3-103">ISCard::Detach method</span></span>

<span data-ttu-id="626a3-104">\[El método **detach** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="626a3-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="626a3-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="626a3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="626a3-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="626a3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="626a3-107">El método **detach** cierra la conexión abierta con la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="626a3-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="626a3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="626a3-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="626a3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="626a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="626a3-110">*Disposición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="626a3-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="626a3-111">Indica qué se debe hacer con la tarjeta en el [*lector*](../secgloss/r-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="626a3-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="626a3-112">Value</span><span class="sxs-lookup"><span data-stu-id="626a3-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="626a3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="626a3-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="626a3-114"><dt>**OMITI**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="626a3-115">Deja la tarjeta inteligente en el [*Estado*](../secgloss/s-gly.md)actual.</span><span class="sxs-lookup"><span data-stu-id="626a3-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="626a3-116"><dt>**DETERMINADO**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="626a3-117">Restablece la tarjeta inteligente a algún estado conocido.</span><span class="sxs-lookup"><span data-stu-id="626a3-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="626a3-118"><dt>**No energía**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="626a3-119">Quita la energía de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="626a3-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="626a3-120"><dt>**EXPULSAR**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="626a3-121">Expulsa la tarjeta inteligente si el lector tiene capacidades de expulsión.</span><span class="sxs-lookup"><span data-stu-id="626a3-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="626a3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="626a3-122">Return value</span></span>

<span data-ttu-id="626a3-123">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="626a3-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="626a3-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="626a3-124">Return code</span></span>                                                                                  | <span data-ttu-id="626a3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="626a3-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="626a3-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="626a3-127">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="626a3-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="626a3-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="626a3-129">La *disposición* no es válida.</span><span class="sxs-lookup"><span data-stu-id="626a3-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="626a3-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="626a3-130">Remarks</span></span>

<span data-ttu-id="626a3-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="626a3-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="626a3-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="626a3-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="626a3-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="626a3-133">Examples</span></span>

<span data-ttu-id="626a3-134">En el ejemplo siguiente se muestra cómo cerrar la conexión con la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="626a3-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="626a3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="626a3-135">Requirements</span></span>



| <span data-ttu-id="626a3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="626a3-136">Requirement</span></span> | <span data-ttu-id="626a3-137">Value</span><span class="sxs-lookup"><span data-stu-id="626a3-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="626a3-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="626a3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="626a3-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="626a3-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="626a3-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="626a3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="626a3-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="626a3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="626a3-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="626a3-142">End of client support</span></span><br/>    | <span data-ttu-id="626a3-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="626a3-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="626a3-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="626a3-144">End of server support</span></span><br/>    | <span data-ttu-id="626a3-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="626a3-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="626a3-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="626a3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="626a3-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="626a3-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="626a3-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="626a3-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="626a3-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="626a3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626a3-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="626a3-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="626a3-152">IID</span><span class="sxs-lookup"><span data-stu-id="626a3-152">IID</span></span><br/>                      | <span data-ttu-id="626a3-153">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="626a3-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="626a3-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="626a3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626a3-155">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="626a3-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="626a3-156">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="626a3-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="626a3-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="626a3-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="626a3-158">**Volver a adjuntar**</span><span class="sxs-lookup"><span data-stu-id="626a3-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
