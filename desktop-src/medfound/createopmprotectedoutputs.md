---
description: Crea objetos de salida protegidos para un dispositivo de pantalla.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539616"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="bcb8a-103">CreateOPMProtectedOutputs función)</span><span class="sxs-lookup"><span data-stu-id="bcb8a-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bcb8a-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="bcb8a-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="bcb8a-106">Crea objetos de salida protegidos para un dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb8a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcb8a-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="bcb8a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcb8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb8a-109">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb8a-110">Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bcb8a-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="bcb8a-111">*vos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb8a-112">Un miembro de la enumeración de **semántica de salida de vídeo de DXGKMDT \_ OPM \_ \_ \_** , que especifica si la salida protegida tendrá semántica de protocolo de protección de salida (COPP) o semántica de OPM.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="bcb8a-113">*dwOPMProtectedOutputArraySize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb8a-114">Número de elementos de la matriz *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="bcb8a-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="bcb8a-115">*pdwNumOPMProtectedOutputsInArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb8a-116">Recibe el número de elementos que la función copia en la matriz *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="bcb8a-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="bcb8a-117">*pohOPMProtectedOutputArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb8a-118">Matriz que recibe los identificadores de los objetos de salida protegidos.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="bcb8a-119">Cada identificador se debe liberar llamando a [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span><span class="sxs-lookup"><span data-stu-id="bcb8a-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb8a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcb8a-120">Return value</span></span>

<span data-ttu-id="bcb8a-121">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="bcb8a-122">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="bcb8a-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb8a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcb8a-123">Remarks</span></span>

<span data-ttu-id="bcb8a-124">En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="bcb8a-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="bcb8a-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="bcb8a-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="bcb8a-126">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="bcb8a-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="bcb8a-127">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-127">This function has no associated import library.</span></span> <span data-ttu-id="bcb8a-128">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="bcb8a-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb8a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb8a-129">Requirements</span></span>



| <span data-ttu-id="bcb8a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb8a-130">Requirement</span></span> | <span data-ttu-id="bcb8a-131">Value</span><span class="sxs-lookup"><span data-stu-id="bcb8a-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb8a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb8a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb8a-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bcb8a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb8a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb8a-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcb8a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bcb8a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bcb8a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcb8a-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb8a-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb8a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcb8a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb8a-139">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="bcb8a-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="bcb8a-140">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="bcb8a-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
