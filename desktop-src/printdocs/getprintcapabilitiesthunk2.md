---
description: Recupera las capacidades de las impresoras con el formato compatible con el esquema de impresión XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706427"
---
# <a name="getprintcapabilitiesthunk2-function"></a><span data-ttu-id="83784-103">GetPrintCapabilitiesThunk2 función)</span><span class="sxs-lookup"><span data-stu-id="83784-103">GetPrintCapabilitiesThunk2 function</span></span>

<span data-ttu-id="83784-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="83784-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="83784-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="83784-105">[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="83784-106">Recupera las capacidades de la impresora con el formato de compatibilidad con el [esquema de impresión](./printschema.md)Xml.</span><span class="sxs-lookup"><span data-stu-id="83784-106">Retrieves the printer's capabilities formatted in compliance with the XML [Print Schema](./printschema.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="83784-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83784-107">Syntax</span></span>


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="83784-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83784-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83784-109">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83784-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-110">Identificador de un proveedor de entradas de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="83784-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="83784-111">La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="83784-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="83784-112">*pPrintTicket* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83784-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-113">El búfer que contiene los datos de los vales de impresión, expresados en XML, tal como se describe en el [esquema de impresión](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="83784-113">The buffer that contains the print ticket data, expressed in XML as described in the [Print Schema](./printschema.md).</span></span>

</dd> <dt>

<span data-ttu-id="83784-114">*cbPrintTicket* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83784-114">*cbPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-115">Tamaño, en bytes, del búfer al que hace referencia *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="83784-115">The size, in bytes, of the buffer referenced by *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="83784-116">*ppbPrintCapabilities* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="83784-116">*ppbPrintCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-117">La dirección del búfer asignado por esta función y contiene la información de funcionalidad de impresión válida, codificada como XML.</span><span class="sxs-lookup"><span data-stu-id="83784-117">The address of the buffer that is allocated by this function and contains the valid print capabilities information, encoded as XML.</span></span> <span data-ttu-id="83784-118">Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer.</span><span class="sxs-lookup"><span data-stu-id="83784-118">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="83784-119">Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="83784-119">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="83784-120">*pcbPrintCapabilitiesLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="83784-120">*pcbPrintCapabilitiesLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-121">Tamaño, en bytes, del búfer al que hace referencia *ppbPrintCapabilities*.</span><span class="sxs-lookup"><span data-stu-id="83784-121">The size, in bytes, of the buffer referenced by *ppbPrintCapabilities*.</span></span>

</dd> <dt>

<span data-ttu-id="83784-122">*pbstrErrorMessage* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="83784-122">*pbstrErrorMessage* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83784-123">Un puntero a una cadena que especifica qué, si no hay nada, no es válido para *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="83784-123">A pointer to a string that specifies what, if anything, is invalid about *pPrintTicket*.</span></span> <span data-ttu-id="83784-124">Si es válido, este valor es **null**.</span><span class="sxs-lookup"><span data-stu-id="83784-124">If it is valid, this value is **NULL**.</span></span> <span data-ttu-id="83784-125">Si *pbstrErrorMessage* no es **null** cuando la función devuelve, el llamador debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="83784-125">If *pbstrErrorMessage* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83784-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83784-126">Return value</span></span>

<span data-ttu-id="83784-127">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83784-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="83784-128">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="83784-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83784-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83784-129">Requirements</span></span>



| <span data-ttu-id="83784-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="83784-130">Requirement</span></span> | <span data-ttu-id="83784-131">Value</span><span class="sxs-lookup"><span data-stu-id="83784-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83784-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83784-132">Minimum supported client</span></span><br/> | <span data-ttu-id="83784-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="83784-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="83784-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83784-134">Minimum supported server</span></span><br/> | <span data-ttu-id="83784-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83784-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83784-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83784-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83784-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83784-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83784-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="83784-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83784-139">**PTGetPrintCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83784-139">**PTGetPrintCapabilities**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[<span data-ttu-id="83784-140">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="83784-140">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="83784-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="83784-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="83784-142">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="83784-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

