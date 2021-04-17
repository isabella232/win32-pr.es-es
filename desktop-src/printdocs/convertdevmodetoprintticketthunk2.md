---
description: Convierte una estructura DEVMODE en una solicitud de impresión.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677725"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a><span data-ttu-id="02215-103">ConvertDevModeToPrintTicketThunk2 función)</span><span class="sxs-lookup"><span data-stu-id="02215-103">ConvertDevModeToPrintTicketThunk2 function</span></span>

<span data-ttu-id="02215-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="02215-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="02215-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="02215-105">[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="02215-106">Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en una solicitud de impresión.</span><span class="sxs-lookup"><span data-stu-id="02215-106">Converts a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to a print ticket.</span></span>

## <a name="syntax"></a><span data-ttu-id="02215-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02215-107">Syntax</span></span>


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a><span data-ttu-id="02215-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02215-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02215-109">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02215-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-110">Identificador de un proveedor de entradas de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="02215-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="02215-111">La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="02215-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="02215-112">*pDevmode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02215-112">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-113">Puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="02215-113">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to convert.</span></span>

</dd> <dt>

<span data-ttu-id="02215-114">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02215-114">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-115">Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado en *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="02215-115">The size, in bytes, of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span>

</dd> <dt>

<span data-ttu-id="02215-116">*ámbito* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="02215-116">*scope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-117">Valor que especifica el ámbito de *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="02215-117">A value that specifies the scope of *ppPrintTicket*.</span></span> <span data-ttu-id="02215-118">Este valor puede especificar una sola página, un documento completo o todos los documentos en el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="02215-118">This value can specify a single page, an entire document, or all documents in the print job.</span></span> <span data-ttu-id="02215-119">El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="02215-119">The value of this parameter must be a member of the [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) enumeration, cast as a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="02215-120">*ppPrintTicket* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02215-120">*ppPrintTicket* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-121">La dirección del búfer que contiene un vale de impresión que representa el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado en *pDevmode*.</span><span class="sxs-lookup"><span data-stu-id="02215-121">The address of the buffer that contains a print ticket that represents the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passed in *pDevmode*.</span></span> <span data-ttu-id="02215-122">Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer.</span><span class="sxs-lookup"><span data-stu-id="02215-122">This function calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate this buffer.</span></span> <span data-ttu-id="02215-123">Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="02215-123">When the buffer is no longer needed, the caller must free it by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="02215-124">*pcbPrintTicketLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02215-124">*pcbPrintTicketLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02215-125">Tamaño, en bytes, de la solicitud de impresión devuelta en *ppPrintTicket*.</span><span class="sxs-lookup"><span data-stu-id="02215-125">The size, in bytes, of the print ticket returned in *ppPrintTicket*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02215-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02215-126">Return value</span></span>

<span data-ttu-id="02215-127">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02215-127">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="02215-128">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="02215-128">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02215-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02215-129">Requirements</span></span>



| <span data-ttu-id="02215-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="02215-130">Requirement</span></span> | <span data-ttu-id="02215-131">Value</span><span class="sxs-lookup"><span data-stu-id="02215-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02215-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02215-132">Minimum supported client</span></span><br/> | <span data-ttu-id="02215-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="02215-133">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="02215-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02215-134">Minimum supported server</span></span><br/> | <span data-ttu-id="02215-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="02215-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="02215-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02215-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02215-137"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02215-137"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02215-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="02215-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02215-139">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="02215-139">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="02215-140">**PTConvertDevModeToPrintTicket**</span><span class="sxs-lookup"><span data-stu-id="02215-140">**PTConvertDevModeToPrintTicket**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[<span data-ttu-id="02215-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="02215-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="02215-142">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="02215-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

