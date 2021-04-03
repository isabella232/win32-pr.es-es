---
title: DestroyPhysicalMonitorInternal función)
description: Cierra un identificador de un monitor físico.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Configuración del monitor de función DestroyPhysicalMonitorInternal
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905221"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="ed798-104">DestroyPhysicalMonitorInternal función)</span><span class="sxs-lookup"><span data-stu-id="ed798-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed798-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ed798-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="ed798-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="ed798-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="ed798-107">Cierra un identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="ed798-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed798-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed798-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="ed798-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed798-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed798-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed798-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed798-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="ed798-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed798-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed798-112">Return value</span></span>

<span data-ttu-id="ed798-113">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ed798-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ed798-114">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="ed798-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed798-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed798-115">Remarks</span></span>

<span data-ttu-id="ed798-116">Las aplicaciones deben llamar a [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="ed798-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="ed798-117">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="ed798-117">This function has no associated import library.</span></span> <span data-ttu-id="ed798-118">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ed798-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed798-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed798-119">Requirements</span></span>



| <span data-ttu-id="ed798-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed798-120">Requirement</span></span> | <span data-ttu-id="ed798-121">Value</span><span class="sxs-lookup"><span data-stu-id="ed798-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed798-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed798-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed798-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed798-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ed798-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed798-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed798-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed798-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed798-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed798-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed798-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed798-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed798-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed798-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed798-129">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="ed798-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

