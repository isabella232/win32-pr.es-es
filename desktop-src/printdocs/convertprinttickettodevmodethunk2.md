---
description: Convierte una solicitud de impresión en una estructura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083025"
---
# <a name="convertprinttickettodevmodethunk2-function"></a><span data-ttu-id="377dd-103">ConvertPrintTicketToDevModeThunk2 función)</span><span class="sxs-lookup"><span data-stu-id="377dd-103">ConvertPrintTicketToDevModeThunk2 function</span></span>

<span data-ttu-id="377dd-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="377dd-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="377dd-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="377dd-105">[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="377dd-106">Convierte una solicitud de impresión en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="377dd-106">Converts a print ticket to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="377dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="377dd-107">Syntax</span></span>


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a><span data-ttu-id="377dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="377dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="377dd-109">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="377dd-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-110">Identificador de un proveedor de entradas de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="377dd-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="377dd-111">La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="377dd-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-112">*pPrintTicket* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="377dd-112">*pPrintTicket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-113">Búfer que contiene el vale de impresión que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="377dd-113">The buffer that contains the print ticket to convert.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-114">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="377dd-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-115">Tamaño, en bytes, del búfer pasado en *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="377dd-115">The size, in bytes, of the buffer passed in *pPrintTicket*.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-116">*BaseType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="377dd-116">*baseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-117">Un valor que indica si el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminado del usuario o el **DEVMODE** predeterminado de la cola de impresión se usa para proporcionar valores al **DEVMODE** de salida cuando *pPrintTicket* no especifica cada valor posible para una estructura **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="377dd-117">A value indicating whether the user's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) or the print queue's default **DEVMODE** is used to provide values to the output **DEVMODE** when *pPrintTicket* does not specify every possible setting for a **DEVMODE**.</span></span> <span data-ttu-id="377dd-118">El valor de este parámetro debe ser un miembro de la enumeración [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , convertido en **int**.</span><span class="sxs-lookup"><span data-stu-id="377dd-118">The value of this parameter must be a member of the [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) enumeration, cast as an **INT**.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-119">*ámbito* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="377dd-119">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-120">Valor que especifica el ámbito de *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="377dd-120">A value that specifies the scope of *pPrintTicket*.</span></span> <span data-ttu-id="377dd-121">Este valor puede especificar una sola página, un documento completo o todos los documentos en el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="377dd-121">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="377dd-122">El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="377dd-122">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-123">*ppDevmode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="377dd-123">*ppDevmode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-124">Dirección del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)recién creado.</span><span class="sxs-lookup"><span data-stu-id="377dd-124">The address of the newly created [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span> <span data-ttu-id="377dd-125">Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer.</span><span class="sxs-lookup"><span data-stu-id="377dd-125">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="377dd-126">Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="377dd-126">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="377dd-127">*pcbDevModeLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="377dd-127">*pcbDevModeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-128">Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelto en *ppDevmode*.</span><span class="sxs-lookup"><span data-stu-id="377dd-128">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) returned in *ppDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="377dd-129">*errMsg* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="377dd-129">*errMsg* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="377dd-130">Un puntero a una cadena que especifica lo que, si hay alguna, no es válido sobre la solicitud de impresión en *pPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="377dd-130">A pointer to a string that specifies what, if anything, is invalid about the print ticket in *pPrintTicket*.</span></span> <span data-ttu-id="377dd-131">Si es válido, es **null**.</span><span class="sxs-lookup"><span data-stu-id="377dd-131">If it is valid, this is **NULL**.</span></span> <span data-ttu-id="377dd-132">Si *errMsg* no es **null** cuando la función devuelve, el llamador debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span><span class="sxs-lookup"><span data-stu-id="377dd-132">If *errMsg* is not **NULL** when the function returns, the caller must free the string with [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="377dd-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="377dd-133">Return value</span></span>

<span data-ttu-id="377dd-134">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="377dd-134">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="377dd-135">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="377dd-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="377dd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="377dd-136">Requirements</span></span>



| <span data-ttu-id="377dd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="377dd-137">Requirement</span></span> | <span data-ttu-id="377dd-138">Value</span><span class="sxs-lookup"><span data-stu-id="377dd-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="377dd-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="377dd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="377dd-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="377dd-140">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="377dd-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="377dd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="377dd-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="377dd-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="377dd-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="377dd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="377dd-144"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="377dd-144"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="377dd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="377dd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377dd-146">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="377dd-146">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="377dd-147">**PTConvertPrintTicketToDevMode**</span><span class="sxs-lookup"><span data-stu-id="377dd-147">**PTConvertPrintTicketToDevMode**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[<span data-ttu-id="377dd-148">Impresión</span><span class="sxs-lookup"><span data-stu-id="377dd-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="377dd-149">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="377dd-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

