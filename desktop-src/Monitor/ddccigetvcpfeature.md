---
title: DDCCIGetVCPFeature función)
description: Obtiene el valor actual, el valor máximo y el tipo de código de un código del panel de control virtual (VCP) de un monitor.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuración del monitor de función DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996364"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="0954d-104">DDCCIGetVCPFeature función)</span><span class="sxs-lookup"><span data-stu-id="0954d-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0954d-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="0954d-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="0954d-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="0954d-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="0954d-107">Obtiene el valor actual, el valor máximo y el tipo de código de un código del panel de control virtual (VCP) de un monitor.</span><span class="sxs-lookup"><span data-stu-id="0954d-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0954d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0954d-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="0954d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0954d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0954d-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0954d-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0954d-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="0954d-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="0954d-112">*dwVCPCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0954d-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0954d-113">Código VCP que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="0954d-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="0954d-114">*pvct* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0954d-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0954d-115">Recibe el tipo de código VCP, como miembro de la enumeración de [**\_ tipo de \_ código \_ MC VCP**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .</span><span class="sxs-lookup"><span data-stu-id="0954d-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0954d-116">*pdwCurrentValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0954d-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0954d-117">Recibe el valor actual del código VCP.</span><span class="sxs-lookup"><span data-stu-id="0954d-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="0954d-118">*pdwMaximumValue* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0954d-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0954d-119">Recibe el valor máximo del código VCP.</span><span class="sxs-lookup"><span data-stu-id="0954d-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0954d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0954d-120">Return value</span></span>

<span data-ttu-id="0954d-121">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0954d-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="0954d-122">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="0954d-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0954d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0954d-123">Remarks</span></span>

<span data-ttu-id="0954d-124">Las aplicaciones deben llamar a [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="0954d-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="0954d-125">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="0954d-125">This function has no associated import library.</span></span> <span data-ttu-id="0954d-126">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="0954d-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0954d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0954d-127">Requirements</span></span>



| <span data-ttu-id="0954d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0954d-128">Requirement</span></span> | <span data-ttu-id="0954d-129">Value</span><span class="sxs-lookup"><span data-stu-id="0954d-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0954d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0954d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0954d-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0954d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0954d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0954d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0954d-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0954d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0954d-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0954d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0954d-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0954d-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0954d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0954d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0954d-137">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="0954d-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

