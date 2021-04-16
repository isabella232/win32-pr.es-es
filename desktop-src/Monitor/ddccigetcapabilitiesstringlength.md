---
title: DDCCIGetCapabilitiesStringLength función)
description: Obtiene la longitud de una cadena de funciones para un monitor.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configuración del monitor de función DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651390"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="8a8af-104">DDCCIGetCapabilitiesStringLength función)</span><span class="sxs-lookup"><span data-stu-id="8a8af-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a8af-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8a8af-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="8a8af-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="8a8af-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="8a8af-107">Obtiene la longitud de una cadena de funciones para un monitor.</span><span class="sxs-lookup"><span data-stu-id="8a8af-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8af-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a8af-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="8a8af-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a8af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8af-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a8af-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8af-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="8a8af-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8a8af-112">*pdwLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a8af-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8af-113">Recibe la longitud de la cadena de funciones, en caracteres, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="8a8af-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8af-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a8af-114">Return value</span></span>

<span data-ttu-id="8a8af-115">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8a8af-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="8a8af-116">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="8a8af-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8af-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a8af-117">Remarks</span></span>

<span data-ttu-id="8a8af-118">Las aplicaciones deben llamar a [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="8a8af-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="8a8af-119">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="8a8af-119">This function has no associated import library.</span></span> <span data-ttu-id="8a8af-120">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8a8af-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8af-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a8af-121">Requirements</span></span>



| <span data-ttu-id="8a8af-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8af-122">Requirement</span></span> | <span data-ttu-id="8a8af-123">Value</span><span class="sxs-lookup"><span data-stu-id="8a8af-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8af-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8af-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a8af-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8a8af-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8af-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a8af-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a8af-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a8af-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8af-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8af-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8af-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a8af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8af-131">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="8a8af-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

