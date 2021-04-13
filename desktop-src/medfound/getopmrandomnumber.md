---
description: Obtiene un número aleatorio seguro criptográficamente de 128 bits de un objeto de salida protegido.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: GetOPMRandomNumber función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360089"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="46121-103">GetOPMRandomNumber función)</span><span class="sxs-lookup"><span data-stu-id="46121-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46121-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="46121-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="46121-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="46121-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="46121-106">Obtiene un número aleatorio seguro criptográficamente de 128 bits de un objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="46121-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46121-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46121-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="46121-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46121-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46121-109">*opoOPMProtectedOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46121-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46121-110">Identificador del objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="46121-110">A handle to the protected output object.</span></span> <span data-ttu-id="46121-111">Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="46121-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="46121-112">*prnRandomNumber* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46121-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46121-113">Puntero a una estructura **de \_ \_ \_ número aleatorio de DXGKMDT OPM** que recibe el número aleatorio.</span><span class="sxs-lookup"><span data-stu-id="46121-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46121-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46121-114">Return value</span></span>

<span data-ttu-id="46121-115">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="46121-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="46121-116">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="46121-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46121-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46121-117">Remarks</span></span>

<span data-ttu-id="46121-118">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="46121-118">This function has no associated import library.</span></span> <span data-ttu-id="46121-119">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="46121-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="46121-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46121-120">Requirements</span></span>



| <span data-ttu-id="46121-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46121-121">Requirement</span></span> | <span data-ttu-id="46121-122">Value</span><span class="sxs-lookup"><span data-stu-id="46121-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46121-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46121-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46121-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46121-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="46121-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46121-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46121-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="46121-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46121-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46121-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46121-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46121-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46121-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="46121-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46121-130">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="46121-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="46121-131">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="46121-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
