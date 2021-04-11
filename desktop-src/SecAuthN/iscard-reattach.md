---
description: El método volver a adjuntar restablece o reinicializa la tarjeta inteligente.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'ISCard:: Reattach (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275917"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="6ccf3-103">ISCard:: Reattach (método)</span><span class="sxs-lookup"><span data-stu-id="6ccf3-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="6ccf3-104">\[El método para volver a **adjuntar** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ccf3-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6ccf3-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6ccf3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6ccf3-107">El método volver a **adjuntar** restablece o reinicializa la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6ccf3-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccf3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ccf3-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="6ccf3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ccf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccf3-110">*ShareMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ccf3-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccf3-111">Modo en el que se va a compartir o es el propietario exclusivo de la conexión a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="6ccf3-112">Value</span><span class="sxs-lookup"><span data-stu-id="6ccf3-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="6ccf3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6ccf3-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="6ccf3-114"><dt>**ÚNICO**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="6ccf3-115">Nadie más usa esta conexión con la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="6ccf3-116"><dt>**RECURSO**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="6ccf3-117">Otras aplicaciones pueden usar esta conexión.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="6ccf3-118">*InitState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ccf3-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccf3-119">Indica qué hacer con la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="6ccf3-120">Value</span><span class="sxs-lookup"><span data-stu-id="6ccf3-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="6ccf3-121">Significado</span><span class="sxs-lookup"><span data-stu-id="6ccf3-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="6ccf3-122"><dt>**OMITI**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="6ccf3-123">Deja la tarjeta inteligente en el [*Estado*](../secgloss/s-gly.md)actual.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="6ccf3-124"><dt>**DETERMINADO**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="6ccf3-125">Restablece la tarjeta inteligente a algún estado conocido.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="6ccf3-126"><dt>**No energía**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="6ccf3-127">Quita la energía de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="6ccf3-128"><dt>**EXPULSAR**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="6ccf3-129">Expulsa la tarjeta inteligente si el lector tiene capacidades de expulsión.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccf3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ccf3-130">Return value</span></span>

<span data-ttu-id="6ccf3-131">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6ccf3-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ccf3-132">Return code</span></span>                                                                                  | <span data-ttu-id="6ccf3-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ccf3-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ccf3-134"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6ccf3-135">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="6ccf3-136"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6ccf3-137">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ccf3-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ccf3-138">Remarks</span></span>

<span data-ttu-id="6ccf3-139">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6ccf3-140">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6ccf3-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6ccf3-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ccf3-141">Examples</span></span>

<span data-ttu-id="6ccf3-142">En el ejemplo siguiente se muestra la reinicialización de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="6ccf3-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6ccf3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccf3-143">Requirements</span></span>



| <span data-ttu-id="6ccf3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccf3-144">Requirement</span></span> | <span data-ttu-id="6ccf3-145">Value</span><span class="sxs-lookup"><span data-stu-id="6ccf3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccf3-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccf3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccf3-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6ccf3-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ccf3-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccf3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccf3-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ccf3-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ccf3-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6ccf3-150">End of client support</span></span><br/>    | <span data-ttu-id="6ccf3-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ccf3-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6ccf3-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6ccf3-152">End of server support</span></span><br/>    | <span data-ttu-id="6ccf3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ccf3-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6ccf3-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ccf3-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccf3-155"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ccf3-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ccf3-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ccf3-157"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ccf3-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ccf3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ccf3-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ccf3-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ccf3-160">IID</span><span class="sxs-lookup"><span data-stu-id="6ccf3-160">IID</span></span><br/>                      | <span data-ttu-id="6ccf3-161">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6ccf3-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6ccf3-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ccf3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccf3-163">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="6ccf3-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="6ccf3-164">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="6ccf3-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="6ccf3-165">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="6ccf3-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="6ccf3-166">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6ccf3-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
