---
title: DDCCISaveCurrentSettings función)
description: Guarda la configuración del monitor actual en el almacenamiento no volátil de la pantalla.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Configuración del monitor de función DDCCISaveCurrentSettings
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996193"
---
# <a name="ddccisavecurrentsettings-function"></a><span data-ttu-id="42c59-104">DDCCISaveCurrentSettings función)</span><span class="sxs-lookup"><span data-stu-id="42c59-104">DDCCISaveCurrentSettings function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42c59-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="42c59-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="42c59-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="42c59-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="42c59-107">Guarda la configuración del monitor actual en el almacenamiento no volátil de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="42c59-107">Saves the current monitor settings to the display's nonvolatile storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c59-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42c59-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="42c59-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42c59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c59-110">*hMonitor*</span><span class="sxs-lookup"><span data-stu-id="42c59-110">*hMonitor*</span></span> 
</dt> <dd>

<span data-ttu-id="42c59-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="42c59-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c59-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42c59-112">Return value</span></span>

<span data-ttu-id="42c59-113">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="42c59-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="42c59-114">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="42c59-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42c59-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42c59-115">Remarks</span></span>

<span data-ttu-id="42c59-116">Las aplicaciones deben llamar a [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="42c59-116">Applications should call [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) instead of calling this function.</span></span>

<span data-ttu-id="42c59-117">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="42c59-117">This function has no associated import library.</span></span> <span data-ttu-id="42c59-118">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="42c59-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42c59-119">Requirements</span></span>



| <span data-ttu-id="42c59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="42c59-120">Requirement</span></span> | <span data-ttu-id="42c59-121">Value</span><span class="sxs-lookup"><span data-stu-id="42c59-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42c59-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42c59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42c59-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42c59-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="42c59-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42c59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42c59-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42c59-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42c59-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42c59-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42c59-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42c59-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c59-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="42c59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c59-129">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="42c59-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

