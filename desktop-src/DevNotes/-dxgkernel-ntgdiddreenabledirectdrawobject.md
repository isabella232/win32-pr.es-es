---
description: Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un cambio de modo.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Función NtGdiDdReenableDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153329"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="dea3b-103">NtGdiDdReenableDirectDrawObject función)</span><span class="sxs-lookup"><span data-stu-id="dea3b-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="dea3b-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dea3b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dea3b-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="dea3b-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dea3b-106">Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un cambio de modo.</span><span class="sxs-lookup"><span data-stu-id="dea3b-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea3b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dea3b-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="dea3b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dea3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea3b-109">*hDirectDrawLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dea3b-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea3b-110">Objeto DirectDraw que debe volver a habilitarse.</span><span class="sxs-lookup"><span data-stu-id="dea3b-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="dea3b-111">*pubNewMode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dea3b-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea3b-112">Puntero a un valor BOOLEANO que se rellenará con un valor que represente si el modo de presentación cambió.</span><span class="sxs-lookup"><span data-stu-id="dea3b-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea3b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dea3b-113">Return value</span></span>

<span data-ttu-id="dea3b-114">Si se realiza correctamente (el dispositivo se puede volver a habilitar), esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="dea3b-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="dea3b-115">En caso contrario (por ejemplo, se ha cambiado el controlador de pantalla), devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="dea3b-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dea3b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dea3b-116">Remarks</span></span>

<span data-ttu-id="dea3b-117">Una vez que se ha vuelto a habilitar el objeto, se pueden volver a consultar las capacidades del dispositivo mediante una llamada a [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span><span class="sxs-lookup"><span data-stu-id="dea3b-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="dea3b-118">Se recomienda que las aplicaciones usen las API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versión 8, que automatizan y abstraen este proceso de forma independiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dea3b-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea3b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea3b-119">Requirements</span></span>



| <span data-ttu-id="dea3b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea3b-120">Requirement</span></span> | <span data-ttu-id="dea3b-121">Value</span><span class="sxs-lookup"><span data-stu-id="dea3b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dea3b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea3b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dea3b-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dea3b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dea3b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea3b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dea3b-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dea3b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dea3b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dea3b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea3b-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea3b-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea3b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dea3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea3b-129">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="dea3b-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="dea3b-130">**DdReenableDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="dea3b-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
