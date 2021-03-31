---
title: DDCCISetVCPFeature función)
description: Establece el valor de un código del panel de control virtual (VCP) para un monitor.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configuración del monitor de función DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150254"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="bfb10-104">DDCCISetVCPFeature función)</span><span class="sxs-lookup"><span data-stu-id="bfb10-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfb10-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="bfb10-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="bfb10-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="bfb10-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="bfb10-107">Establece el valor de un código del panel de control virtual (VCP) para un monitor.</span><span class="sxs-lookup"><span data-stu-id="bfb10-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfb10-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="bfb10-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfb10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb10-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfb10-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb10-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="bfb10-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="bfb10-112">*dwVCPCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfb10-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb10-113">Código VCP que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="bfb10-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="bfb10-114">*dwNewValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfb10-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb10-115">Valor del código VCP.</span><span class="sxs-lookup"><span data-stu-id="bfb10-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb10-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfb10-116">Return value</span></span>

<span data-ttu-id="bfb10-117">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bfb10-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="bfb10-118">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="bfb10-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb10-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb10-119">Remarks</span></span>

<span data-ttu-id="bfb10-120">Las aplicaciones deben llamar a [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="bfb10-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="bfb10-121">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="bfb10-121">This function has no associated import library.</span></span> <span data-ttu-id="bfb10-122">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="bfb10-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb10-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb10-123">Requirements</span></span>



| <span data-ttu-id="bfb10-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb10-124">Requirement</span></span> | <span data-ttu-id="bfb10-125">Value</span><span class="sxs-lookup"><span data-stu-id="bfb10-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb10-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb10-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb10-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bfb10-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfb10-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb10-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb10-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfb10-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfb10-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfb10-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfb10-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfb10-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb10-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfb10-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb10-133">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="bfb10-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

