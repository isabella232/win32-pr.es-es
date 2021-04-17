---
description: Cierra un identificador de un proveedor de entradas de impresión.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697150"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="239a0-103">UnbindPTProviderThunk función)</span><span class="sxs-lookup"><span data-stu-id="239a0-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="239a0-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="239a0-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="239a0-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="239a0-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="239a0-106">Cierra un identificador de un proveedor de entradas de impresión.</span><span class="sxs-lookup"><span data-stu-id="239a0-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="239a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="239a0-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="239a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="239a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239a0-109">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="239a0-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="239a0-110">Identificador de un proveedor de entradas de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="239a0-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="239a0-111">La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="239a0-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239a0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="239a0-112">Return value</span></span>

<span data-ttu-id="239a0-113">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="239a0-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="239a0-114">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="239a0-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="239a0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="239a0-115">Requirements</span></span>



| <span data-ttu-id="239a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="239a0-116">Requirement</span></span> | <span data-ttu-id="239a0-117">Value</span><span class="sxs-lookup"><span data-stu-id="239a0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="239a0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="239a0-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="239a0-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="239a0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="239a0-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="239a0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="239a0-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="239a0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="239a0-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="239a0-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239a0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="239a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239a0-125">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="239a0-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="239a0-126">**PTCloseProvider**</span><span class="sxs-lookup"><span data-stu-id="239a0-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="239a0-127">Impresión</span><span class="sxs-lookup"><span data-stu-id="239a0-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="239a0-128">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="239a0-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

