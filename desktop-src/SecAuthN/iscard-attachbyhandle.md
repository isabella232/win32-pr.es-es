---
description: Adjunta el objeto ISCard a un identificador de tarjeta inteligente abierto y configurado.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'ISCard:: AttachByHandle (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649182"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="87652-103">ISCard:: AttachByHandle (método)</span><span class="sxs-lookup"><span data-stu-id="87652-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="87652-104">\[El método **AttachByHandle** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="87652-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87652-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87652-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="87652-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="87652-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="87652-107">El método **AttachByHandle** asocia el objeto [**ISCard**](iscard.md) a un identificador de [*tarjeta inteligente*](../secgloss/s-gly.md) abierto y configurado.</span><span class="sxs-lookup"><span data-stu-id="87652-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="87652-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87652-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="87652-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87652-110">*hCard* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87652-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87652-111">Identificador de una conexión abierta a una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="87652-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87652-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87652-112">Return value</span></span>

<span data-ttu-id="87652-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="87652-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="87652-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="87652-114">Return code</span></span>                                                                                  | <span data-ttu-id="87652-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="87652-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="87652-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="87652-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="87652-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="87652-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="87652-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="87652-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="87652-119">El parámetro *hCard* no es válido.</span><span class="sxs-lookup"><span data-stu-id="87652-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87652-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87652-120">Remarks</span></span>

<span data-ttu-id="87652-121">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87652-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="87652-122">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="87652-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="87652-123">Cuando haya terminado de usar el identificador, libere los datos adjuntos llamando al método [**ISCard::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="87652-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="87652-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="87652-124">Examples</span></span>

<span data-ttu-id="87652-125">En el ejemplo siguiente se muestra cómo conectarse a un identificador de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="87652-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="87652-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87652-126">Requirements</span></span>



| <span data-ttu-id="87652-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87652-127">Requirement</span></span> | <span data-ttu-id="87652-128">Value</span><span class="sxs-lookup"><span data-stu-id="87652-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87652-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87652-129">Minimum supported client</span></span><br/> | <span data-ttu-id="87652-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="87652-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87652-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87652-131">Minimum supported server</span></span><br/> | <span data-ttu-id="87652-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="87652-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87652-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="87652-133">End of client support</span></span><br/>    | <span data-ttu-id="87652-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="87652-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="87652-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="87652-135">End of server support</span></span><br/>    | <span data-ttu-id="87652-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87652-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="87652-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87652-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="87652-138"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="87652-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="87652-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="87652-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="87652-140"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87652-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87652-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87652-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87652-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87652-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87652-143">IID</span><span class="sxs-lookup"><span data-stu-id="87652-143">IID</span></span><br/>                      | <span data-ttu-id="87652-144">IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="87652-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="87652-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="87652-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87652-146">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="87652-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="87652-147">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="87652-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="87652-148">**obtener \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="87652-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="87652-149">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="87652-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="87652-150">**Volver a adjuntar**</span><span class="sxs-lookup"><span data-stu-id="87652-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
