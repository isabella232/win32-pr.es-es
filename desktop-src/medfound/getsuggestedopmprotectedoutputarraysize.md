---
description: Obtiene el tamaño de la matriz que se debe asignar antes de llamar a CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153626"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="e08d3-103">GetSuggestedOPMProtectedOutputArraySize función)</span><span class="sxs-lookup"><span data-stu-id="e08d3-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e08d3-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e08d3-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e08d3-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e08d3-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e08d3-106">Obtiene el tamaño de la matriz que se debe asignar antes de llamar a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="e08d3-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e08d3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e08d3-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="e08d3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e08d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e08d3-109">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e08d3-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08d3-110">Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e08d3-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e08d3-111">*pdwSuggestedOPMProtectedOutputArraySize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e08d3-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e08d3-112">Recibe el tamaño que se debe asignar para la matriz, en número de elementos de matriz.</span><span class="sxs-lookup"><span data-stu-id="e08d3-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e08d3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e08d3-113">Return value</span></span>

<span data-ttu-id="e08d3-114">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e08d3-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e08d3-115">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e08d3-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e08d3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e08d3-116">Remarks</span></span>

<span data-ttu-id="e08d3-117">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="e08d3-117">This function has no associated import library.</span></span> <span data-ttu-id="e08d3-118">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e08d3-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08d3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08d3-119">Requirements</span></span>



| <span data-ttu-id="e08d3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08d3-120">Requirement</span></span> | <span data-ttu-id="e08d3-121">Value</span><span class="sxs-lookup"><span data-stu-id="e08d3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e08d3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e08d3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e08d3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e08d3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e08d3-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e08d3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e08d3-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e08d3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08d3-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08d3-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08d3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e08d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08d3-129">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="e08d3-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e08d3-130">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="e08d3-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
