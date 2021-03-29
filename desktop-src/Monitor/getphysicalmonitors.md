---
title: GetPhysicalMonitors función)
description: Obtiene los monitores físicos asociados a un dispositivo de pantalla.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configuración del monitor de función GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665989"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="2e9e1-104">GetPhysicalMonitors función)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e9e1-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="2e9e1-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="2e9e1-107">Obtiene los monitores físicos asociados a un dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e9e1-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="2e9e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e9e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9e1-110">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-111">Puntero a una estructura de [**\_ cadena Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="2e9e1-112">*dwPhysicalMonitorArraySize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-113">Número de elementos de la matriz *pdwNumPhysicalMonitorHandlesInArray* .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="2e9e1-114">Para obtener el tamaño necesario de la matriz, llame a [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="2e9e1-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e9e1-115">*pdwNumPhysicalMonitorHandlesInArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-116">Recibe el número de elementos que la función copia en la matriz *phPhysicalMonitorArray* .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="2e9e1-117">*phPhysicalMonitorArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-118">Matriz que recibe los identificadores de los monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="2e9e1-119">Cada identificador se debe liberar llamando a [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span><span class="sxs-lookup"><span data-stu-id="2e9e1-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9e1-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e9e1-120">Return value</span></span>

<span data-ttu-id="2e9e1-121">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="2e9e1-122">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="2e9e1-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e9e1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e9e1-123">Remarks</span></span>

<span data-ttu-id="2e9e1-124">En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="2e9e1-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="2e9e1-125">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="2e9e1-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="2e9e1-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="2e9e1-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="2e9e1-127">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-127">This function has no associated import library.</span></span> <span data-ttu-id="2e9e1-128">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9e1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e9e1-129">Requirements</span></span>



| <span data-ttu-id="2e9e1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e9e1-130">Requirement</span></span> | <span data-ttu-id="2e9e1-131">Value</span><span class="sxs-lookup"><span data-stu-id="2e9e1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9e1-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e9e1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9e1-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2e9e1-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e9e1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9e1-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2e9e1-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e9e1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e9e1-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e9e1-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9e1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e9e1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9e1-139">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="2e9e1-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

