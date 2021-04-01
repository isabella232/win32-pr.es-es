---
title: DDCCIGetTimingReport función)
description: Obtiene las frecuencias de sincronización horizontal y vertical de un monitor.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configuración del monitor de función DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996365"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="d9b1b-104">DDCCIGetTimingReport función)</span><span class="sxs-lookup"><span data-stu-id="d9b1b-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9b1b-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="d9b1b-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="d9b1b-107">Obtiene las frecuencias de sincronización horizontal y vertical de un monitor.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b1b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9b1b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="d9b1b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9b1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b1b-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9b1b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b1b-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d9b1b-112">*PMTR* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d9b1b-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b1b-113">Puntero a una estructura [**de \_ \_ Informe de temporización de MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) que recibe la información de control de tiempo.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b1b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9b1b-114">Return value</span></span>

<span data-ttu-id="d9b1b-115">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d9b1b-116">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d9b1b-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b1b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9b1b-117">Remarks</span></span>

<span data-ttu-id="d9b1b-118">Las aplicaciones deben llamar a [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="d9b1b-119">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-119">This function has no associated import library.</span></span> <span data-ttu-id="d9b1b-120">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d9b1b-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9b1b-121">Requirements</span></span>



| <span data-ttu-id="d9b1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b1b-122">Requirement</span></span> | <span data-ttu-id="d9b1b-123">Value</span><span class="sxs-lookup"><span data-stu-id="d9b1b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b1b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9b1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b1b-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9b1b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d9b1b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9b1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b1b-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9b1b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9b1b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9b1b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9b1b-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1b-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b1b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9b1b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b1b-131">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="d9b1b-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

