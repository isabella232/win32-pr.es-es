---
description: Libera una estructura de contexto de firmante \_ asignada por una llamada anterior a la función SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667905"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="05bcc-103">SignerFreeSignerContext función)</span><span class="sxs-lookup"><span data-stu-id="05bcc-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="05bcc-104">La función **SignerFreeSignerContext** libera una estructura de [**\_ contexto de firmante**](signer-context.md) asignada por una llamada anterior a la función [**SignerSignEx**](signersignex.md) .</span><span class="sxs-lookup"><span data-stu-id="05bcc-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="05bcc-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="05bcc-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="05bcc-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="05bcc-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="05bcc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05bcc-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="05bcc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05bcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05bcc-109">*pSignerContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05bcc-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05bcc-110">Puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="05bcc-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05bcc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05bcc-111">Return value</span></span>

<span data-ttu-id="05bcc-112">Si la función se ejecuta correctamente, la función devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05bcc-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="05bcc-113">Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="05bcc-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="05bcc-114">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="05bcc-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05bcc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05bcc-115">Requirements</span></span>



| <span data-ttu-id="05bcc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="05bcc-116">Requirement</span></span> | <span data-ttu-id="05bcc-117">Value</span><span class="sxs-lookup"><span data-stu-id="05bcc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05bcc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05bcc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05bcc-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="05bcc-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="05bcc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05bcc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05bcc-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="05bcc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05bcc-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05bcc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05bcc-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05bcc-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bcc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="05bcc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bcc-125">**contexto del firmante \_**</span><span class="sxs-lookup"><span data-stu-id="05bcc-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="05bcc-126">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="05bcc-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
