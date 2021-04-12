---
description: El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un acoplamiento o desacoplamiento. Una aplicación o un controlador que almacene datos en el registro con la clave de configuración de HKEY \_ Current \_ debe actualizar los datos.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Evento DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274958"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="380a9-104">\_Evento DBT CONFIGCHANGED</span><span class="sxs-lookup"><span data-stu-id="380a9-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="380a9-105">El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGED para indicar que la configuración actual ha cambiado, debido a un acoplamiento o desacoplamiento.</span><span class="sxs-lookup"><span data-stu-id="380a9-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="380a9-106">Una aplicación o un controlador que almacene datos en el registro con la clave de configuración de HKEY \_ Current \_ debe actualizar los datos.</span><span class="sxs-lookup"><span data-stu-id="380a9-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="380a9-107">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ CONFIGCHANGED y *lParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="380a9-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="380a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="380a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380a9-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="380a9-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="380a9-110">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="380a9-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="380a9-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="380a9-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="380a9-112">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="380a9-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="380a9-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="380a9-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="380a9-114">Establézcalo en DBT \_ CONFIGCHANGED.</span><span class="sxs-lookup"><span data-stu-id="380a9-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="380a9-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="380a9-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="380a9-116">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="380a9-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380a9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="380a9-117">Return value</span></span>

<span data-ttu-id="380a9-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="380a9-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="380a9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380a9-119">Requirements</span></span>



| <span data-ttu-id="380a9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="380a9-120">Requirement</span></span> | <span data-ttu-id="380a9-121">Value</span><span class="sxs-lookup"><span data-stu-id="380a9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="380a9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="380a9-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="380a9-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="380a9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="380a9-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="380a9-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="380a9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="380a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="380a9-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="380a9-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="380a9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="380a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380a9-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="380a9-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="380a9-130">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="380a9-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="380a9-131">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="380a9-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




