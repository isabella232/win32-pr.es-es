---
description: Abre una instancia de un proveedor de entradas de impresión.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276670"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="407d9-103">BindPTProviderThunk función)</span><span class="sxs-lookup"><span data-stu-id="407d9-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="407d9-104">\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="407d9-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="407d9-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="407d9-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="407d9-106">Abre una instancia de un proveedor de entradas de impresión.</span><span class="sxs-lookup"><span data-stu-id="407d9-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="407d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="407d9-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="407d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="407d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="407d9-109">*pszPrinterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="407d9-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="407d9-110">Nombre completo de una cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="407d9-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="407d9-111">*MaxVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="407d9-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="407d9-112">La versión más reciente del [esquema de impresión](./printschema.md) que admite el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="407d9-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="407d9-113">*prefVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="407d9-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="407d9-114">Versión del esquema de [impresión](./printschema.md) solicitado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="407d9-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="407d9-115">*phProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="407d9-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="407d9-116">Un puntero a un identificador para el proveedor de entradas de impresión.</span><span class="sxs-lookup"><span data-stu-id="407d9-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="407d9-117">*usedVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="407d9-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="407d9-118">Versión del esquema de [impresión](./printschema.md) que utilizará el proveedor de entradas de impresión.</span><span class="sxs-lookup"><span data-stu-id="407d9-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="407d9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="407d9-119">Return value</span></span>

<span data-ttu-id="407d9-120">Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="407d9-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="407d9-121">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="407d9-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="407d9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="407d9-122">Remarks</span></span>

<span data-ttu-id="407d9-123">Antes de llamar a esta función, el subproceso que realiza la llamada debe inicializar COM llamando a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="407d9-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="407d9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407d9-124">Requirements</span></span>



| <span data-ttu-id="407d9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="407d9-125">Requirement</span></span> | <span data-ttu-id="407d9-126">Value</span><span class="sxs-lookup"><span data-stu-id="407d9-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="407d9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="407d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="407d9-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="407d9-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="407d9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="407d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="407d9-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="407d9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="407d9-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="407d9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="407d9-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="407d9-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="407d9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="407d9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407d9-134">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="407d9-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="407d9-135">**PTOpenProviderEx**</span><span class="sxs-lookup"><span data-stu-id="407d9-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="407d9-136">Impresión</span><span class="sxs-lookup"><span data-stu-id="407d9-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="407d9-137">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="407d9-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

