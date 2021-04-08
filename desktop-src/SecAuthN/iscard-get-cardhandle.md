---
description: Recupera el identificador de una tarjeta inteligente conectada. Este método devuelve ( \* pHandle) = = NULL si no está conectado.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Método ISCard:: get_CardHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000917"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="34419-104">ISCard:: get \_ CardHandle (método)</span><span class="sxs-lookup"><span data-stu-id="34419-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="34419-105">\[El método **Get \_ CardHandle** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="34419-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="34419-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="34419-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="34419-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="34419-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="34419-108">El método **Get \_ CardHandle** recupera el identificador de una [*tarjeta inteligente*](../secgloss/s-gly.md)conectada.</span><span class="sxs-lookup"><span data-stu-id="34419-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="34419-109">Este método devuelve ( \* pHandle) = = **null** si no está conectado.</span><span class="sxs-lookup"><span data-stu-id="34419-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="34419-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34419-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="34419-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34419-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34419-112">*pHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34419-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34419-113">Puntero al identificador de la tarjeta en la devolución.</span><span class="sxs-lookup"><span data-stu-id="34419-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34419-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34419-114">Return value</span></span>

<span data-ttu-id="34419-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="34419-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="34419-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="34419-116">Return code</span></span>                                                                                  | <span data-ttu-id="34419-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="34419-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="34419-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="34419-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="34419-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="34419-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="34419-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="34419-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="34419-121">El parámetro *pHandle* no es válido.</span><span class="sxs-lookup"><span data-stu-id="34419-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="34419-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="34419-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="34419-123">Se pasó un puntero no válido en *pHandle*.</span><span class="sxs-lookup"><span data-stu-id="34419-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34419-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34419-124">Remarks</span></span>

<span data-ttu-id="34419-125">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34419-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="34419-126">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="34419-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="34419-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="34419-127">Examples</span></span>

<span data-ttu-id="34419-128">En el ejemplo siguiente se muestra cómo recuperar el identificador de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="34419-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="34419-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34419-129">Requirements</span></span>



| <span data-ttu-id="34419-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="34419-130">Requirement</span></span> | <span data-ttu-id="34419-131">Value</span><span class="sxs-lookup"><span data-stu-id="34419-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34419-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34419-132">Minimum supported client</span></span><br/> | <span data-ttu-id="34419-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="34419-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="34419-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34419-134">Minimum supported server</span></span><br/> | <span data-ttu-id="34419-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34419-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34419-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="34419-136">End of client support</span></span><br/>    | <span data-ttu-id="34419-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34419-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="34419-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="34419-138">End of server support</span></span><br/>    | <span data-ttu-id="34419-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34419-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="34419-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34419-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="34419-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="34419-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="34419-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="34419-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="34419-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34419-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34419-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34419-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34419-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34419-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34419-146">IID</span><span class="sxs-lookup"><span data-stu-id="34419-146">IID</span></span><br/>                      | <span data-ttu-id="34419-147">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="34419-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="34419-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="34419-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34419-149">**obtener \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="34419-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="34419-150">**obtener \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="34419-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="34419-151">**obtener \_ Protocolo**</span><span class="sxs-lookup"><span data-stu-id="34419-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="34419-152">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="34419-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="34419-153">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="34419-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
