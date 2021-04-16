---
description: Libera un objeto de salida protegido.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: DestroyOPMProtectedOutput función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686466"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="806a5-103">DestroyOPMProtectedOutput función)</span><span class="sxs-lookup"><span data-stu-id="806a5-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="806a5-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="806a5-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="806a5-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="806a5-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="806a5-106">Libera un objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="806a5-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="806a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="806a5-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="806a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="806a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806a5-109">*opoOPMProtectedOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="806a5-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806a5-110">Identificador del objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="806a5-110">A handle to the protected output object.</span></span> <span data-ttu-id="806a5-111">Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="806a5-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806a5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="806a5-112">Return value</span></span>

<span data-ttu-id="806a5-113">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="806a5-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="806a5-114">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="806a5-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="806a5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="806a5-115">Remarks</span></span>

<span data-ttu-id="806a5-116">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="806a5-116">This function has no associated import library.</span></span> <span data-ttu-id="806a5-117">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="806a5-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="806a5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806a5-118">Requirements</span></span>



| <span data-ttu-id="806a5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="806a5-119">Requirement</span></span> | <span data-ttu-id="806a5-120">Value</span><span class="sxs-lookup"><span data-stu-id="806a5-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="806a5-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="806a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="806a5-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="806a5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="806a5-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="806a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="806a5-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="806a5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="806a5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="806a5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="806a5-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="806a5-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806a5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="806a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806a5-128">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="806a5-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="806a5-129">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="806a5-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
