---
title: GetNumberOfPhysicalMonitors función)
description: Obtiene el número de monitores físicos asociados a un dispositivo de pantalla.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configuración del monitor de función GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905220"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="df9ba-104">GetNumberOfPhysicalMonitors función)</span><span class="sxs-lookup"><span data-stu-id="df9ba-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df9ba-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="df9ba-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="df9ba-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="df9ba-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="df9ba-107">Obtiene el número de monitores físicos asociados a un dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="df9ba-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9ba-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df9ba-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="df9ba-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df9ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9ba-110">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df9ba-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9ba-111">Puntero a una estructura de [**\_ cadena Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="df9ba-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="df9ba-112">*pdwNumberOfPhysicalMonitors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="df9ba-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df9ba-113">Recibe el número de monitores físicos.</span><span class="sxs-lookup"><span data-stu-id="df9ba-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9ba-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df9ba-114">Return value</span></span>

<span data-ttu-id="df9ba-115">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="df9ba-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="df9ba-116">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="df9ba-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="df9ba-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df9ba-117">Remarks</span></span>

<span data-ttu-id="df9ba-118">En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="df9ba-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="df9ba-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="df9ba-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="df9ba-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="df9ba-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="df9ba-121">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="df9ba-121">This function has no associated import library.</span></span> <span data-ttu-id="df9ba-122">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="df9ba-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9ba-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df9ba-123">Requirements</span></span>



| <span data-ttu-id="df9ba-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="df9ba-124">Requirement</span></span> | <span data-ttu-id="df9ba-125">Value</span><span class="sxs-lookup"><span data-stu-id="df9ba-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df9ba-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="df9ba-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df9ba-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="df9ba-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df9ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="df9ba-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df9ba-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="df9ba-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df9ba-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df9ba-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df9ba-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df9ba-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="df9ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9ba-133">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="df9ba-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

