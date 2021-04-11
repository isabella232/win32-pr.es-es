---
description: Establece la rampa gamma del dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Función NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152806"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="1a515-103">NtGdiDdSetGammaRamp función)</span><span class="sxs-lookup"><span data-stu-id="1a515-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="1a515-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a515-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1a515-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="1a515-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1a515-106">Establece la rampa gamma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a515-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a515-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a515-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="1a515-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a515-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a515-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a515-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a515-110">Identificador del objeto de controlador de modo kernel para el que se va a establecer la rampa.</span><span class="sxs-lookup"><span data-stu-id="1a515-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="1a515-111">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a515-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a515-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1a515-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1a515-113">*lpGammaRamp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a515-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a515-114">Puntero a una matriz de estructuras **DDGAMMARAMP** .</span><span class="sxs-lookup"><span data-stu-id="1a515-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a515-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a515-115">Return value</span></span>

<span data-ttu-id="1a515-116">El valor devuelto es **true** si la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a515-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="1a515-117">De lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="1a515-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a515-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a515-118">Remarks</span></span>

<span data-ttu-id="1a515-119">Se recomienda que las aplicaciones usen los métodos **IDirectDrawGammaControl:: SetGammaRamp** o [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) en su lugar porque estos métodos ofrecen la misma funcionalidad independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a515-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a515-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a515-120">Requirements</span></span>



| <span data-ttu-id="1a515-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a515-121">Requirement</span></span> | <span data-ttu-id="1a515-122">Value</span><span class="sxs-lookup"><span data-stu-id="1a515-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a515-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a515-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a515-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1a515-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1a515-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a515-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a515-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a515-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1a515-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a515-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a515-128"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a515-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a515-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a515-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a515-130">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="1a515-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
