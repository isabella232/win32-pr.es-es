---
description: Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688576"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a><span data-ttu-id="c5186-103">MergeAndValidatePrintTicketThunk2 función)</span><span class="sxs-lookup"><span data-stu-id="c5186-103">MergeAndValidatePrintTicketThunk2 function</span></span>

<span data-ttu-id="c5186-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="c5186-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="c5186-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="c5186-105">[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="c5186-106">Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.</span><span class="sxs-lookup"><span data-stu-id="c5186-106">Merges two print tickets and returns a valid, viable print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5186-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5186-107">Syntax</span></span>


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="c5186-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5186-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5186-109">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5186-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-110">Identificador de un proveedor de entradas de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="c5186-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="c5186-111">La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="c5186-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-112">*pBasePrintTicket* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5186-112">*pBasePrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-113">Búfer que contiene los datos de los vales de impresión base, expresados en XML, tal como se describe en el [esquema de impresión](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="c5186-113">The buffer that contains the base print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5186-114">*basePrintTicketLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5186-114">*basePrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-115">Tamaño, en bytes, del búfer al que hace referencia *pBasePrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="c5186-115">The size, in bytes, of the buffer referenced by *pBasePrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-116">*pDeltaPrintTicket* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c5186-116">*pDeltaPrintTicket* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-117">Búfer que contiene el vale de impresión que se va a combinar.</span><span class="sxs-lookup"><span data-stu-id="c5186-117">The buffer that contains the print ticket to merge.</span></span> <span data-ttu-id="c5186-118">Los datos de los vales de impresión se expresan en XML tal y como se describe en el [esquema de impresión](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="c5186-118">The print ticket data is expressed in XML as described in the [Print Schema](./printschema.md).</span></span> <span data-ttu-id="c5186-119">El valor de este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c5186-119">The value of this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-120">*deltaPrintTicketLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5186-120">*deltaPrintTicketLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-121">Tamaño, en bytes, del búfer al que hace referencia *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="c5186-121">The size, in bytes, of the buffer referenced by *pDeltaPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-122">*ámbito* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c5186-122">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-123">Valor que especifica si el ámbito de *pDeltaPrintTicket* y *ppValidatedPrintTicket* es una sola página, un documento completo o todos los documentos en el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c5186-123">The value that specifies whether the scope of *pDeltaPrintTicket* and *ppValidatedPrintTicket* is a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="c5186-124">El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c5186-124">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-125">*ppValidatedPrintTicket* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5186-125">*ppValidatedPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-126">La dirección del búfer que contiene la solicitud de impresión combinada y validada.</span><span class="sxs-lookup"><span data-stu-id="c5186-126">The address of the buffer that contains the merged and validated print ticket.</span></span> <span data-ttu-id="c5186-127">Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer.</span><span class="sxs-lookup"><span data-stu-id="c5186-127">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="c5186-128">Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="c5186-128">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="c5186-129">*pValidatedPrintTicketLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5186-129">*pValidatedPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-130">Tamaño, en bytes, del búfer al que hace referencia *ppValidatedPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="c5186-130">The size, in bytes, of the buffer referenced by *ppValidatedPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="c5186-131">*pbstrErrorMessage* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c5186-131">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5186-132">Un puntero a una cadena que especifica lo que, si hay alguna, no es válido sobre la solicitud de impresión en *pBasePrintTicket* o *pDeltaPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="c5186-132">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pBasePrintTicket* or *pDeltaPrintTicket*.</span></span> <span data-ttu-id="c5186-133">Si ambos son válidos, este valor es **null**.</span><span class="sxs-lookup"><span data-stu-id="c5186-133">If they are both valid, this value is **NULL**.</span></span> <span data-ttu-id="c5186-134">Si *pbstrErrorMessage* no es **null** cuando la función devuelve, el llamador debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="c5186-134">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5186-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5186-135">Return value</span></span>

<span data-ttu-id="c5186-136">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5186-136">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="c5186-137">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="c5186-137">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5186-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5186-138">Requirements</span></span>



| <span data-ttu-id="c5186-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5186-139">Requirement</span></span> | <span data-ttu-id="c5186-140">Value</span><span class="sxs-lookup"><span data-stu-id="c5186-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5186-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5186-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c5186-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c5186-142">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c5186-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5186-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c5186-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5186-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c5186-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5186-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5186-146"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5186-146"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5186-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5186-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5186-148">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="c5186-148">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="c5186-149">**PTMergeAndValidatePrintTicket**</span><span class="sxs-lookup"><span data-stu-id="c5186-149">**PTMergeAndValidatePrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[<span data-ttu-id="c5186-150">Impresión</span><span class="sxs-lookup"><span data-stu-id="c5186-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c5186-151">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="c5186-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

