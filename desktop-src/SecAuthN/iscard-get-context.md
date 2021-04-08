---
description: Recupera el identificador de contexto del administrador de recursos actual. Este método devuelve ( \* pContext) = = NULL si no se ha establecido ningún contexto.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Método ISCard:: get_Context (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912469"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="a2ab0-104">ISCard:: get ( \_ método de contexto)</span><span class="sxs-lookup"><span data-stu-id="a2ab0-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="a2ab0-105">\[El método de **\_ contexto Get** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2ab0-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2ab0-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a2ab0-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a2ab0-108">El método de **\_ contexto Get** recupera el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="a2ab0-109">Este método devuelve ( \* *pContext*) = = **null** si no se ha establecido ningún contexto.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ab0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2ab0-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="a2ab0-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2ab0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ab0-112">*pContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a2ab0-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ab0-113">Puntero al identificador de contexto en la devolución.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ab0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2ab0-114">Return value</span></span>

<span data-ttu-id="a2ab0-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a2ab0-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a2ab0-116">Return code</span></span>                                                                                  | <span data-ttu-id="a2ab0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2ab0-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="a2ab0-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a2ab0-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="a2ab0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a2ab0-121">El parámetro *pContext* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a2ab0-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a2ab0-123">Se pasó un puntero incorrecto en *pContext*.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2ab0-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2ab0-124">Remarks</span></span>

<span data-ttu-id="a2ab0-125">El contexto del administrador de recursos se establece mediante una llamada a la función de [*tarjeta inteligente*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span><span class="sxs-lookup"><span data-stu-id="a2ab0-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="a2ab0-126">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a2ab0-127">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a2ab0-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a2ab0-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a2ab0-128">Examples</span></span>

<span data-ttu-id="a2ab0-129">En el ejemplo siguiente se muestra cómo recuperar el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual.</span><span class="sxs-lookup"><span data-stu-id="a2ab0-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="a2ab0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ab0-130">Requirements</span></span>



| <span data-ttu-id="a2ab0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ab0-131">Requirement</span></span> | <span data-ttu-id="a2ab0-132">Value</span><span class="sxs-lookup"><span data-stu-id="a2ab0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ab0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2ab0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ab0-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a2ab0-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2ab0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2ab0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ab0-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2ab0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2ab0-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a2ab0-137">End of client support</span></span><br/>    | <span data-ttu-id="a2ab0-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2ab0-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a2ab0-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a2ab0-139">End of server support</span></span><br/>    | <span data-ttu-id="a2ab0-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2ab0-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a2ab0-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2ab0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ab0-142"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2ab0-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a2ab0-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2ab0-144"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2ab0-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2ab0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ab0-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ab0-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2ab0-147">IID</span><span class="sxs-lookup"><span data-stu-id="a2ab0-147">IID</span></span><br/>                      | <span data-ttu-id="a2ab0-148">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a2ab0-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a2ab0-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2ab0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ab0-150">**obtener \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="a2ab0-151">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="a2ab0-152">**obtener \_ Protocolo**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="a2ab0-153">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="a2ab0-154">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="a2ab0-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="a2ab0-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
