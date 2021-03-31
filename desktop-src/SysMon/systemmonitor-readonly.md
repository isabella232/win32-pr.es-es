---
title: SystemMonitor. ReadOnly (propiedad)
description: Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propiedad de solo lectura SysMon
- Propiedad de solo lectura SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996351"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="d0ac6-106">SystemMonitor. ReadOnly (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d0ac6-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="d0ac6-107">Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="d0ac6-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ac6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0ac6-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d0ac6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d0ac6-110">Property value</span></span>

<span data-ttu-id="d0ac6-111">True si no se desea que el usuario modifique los valores de propiedad del control; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="d0ac6-112">El valor predeterminado es false, lo que significa que los usuarios pueden modificar los valores de propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ac6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0ac6-113">Remarks</span></span>

<span data-ttu-id="d0ac6-114">Cuando el valor de esta propiedad es true, se aplican las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="d0ac6-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="d0ac6-115">El usuario no puede utilizar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="d0ac6-116">Los siguientes botones de la barra de herramientas están deshabilitados:</span><span class="sxs-lookup"><span data-stu-id="d0ac6-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="d0ac6-117">Nuevo conjunto de contadores</span><span class="sxs-lookup"><span data-stu-id="d0ac6-117">New Counter Set</span></span>
    -   <span data-ttu-id="d0ac6-118">Ver la actividad actual</span><span class="sxs-lookup"><span data-stu-id="d0ac6-118">View Current Activity</span></span>
    -   <span data-ttu-id="d0ac6-119">Ver datos del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="d0ac6-119">View Log File Data</span></span>
    -   <span data-ttu-id="d0ac6-120">Sumar</span><span class="sxs-lookup"><span data-stu-id="d0ac6-120">Add</span></span>
    -   <span data-ttu-id="d0ac6-121">Eliminar</span><span class="sxs-lookup"><span data-stu-id="d0ac6-121">Delete</span></span>
    -   <span data-ttu-id="d0ac6-122">Pegar lista de contadores</span><span class="sxs-lookup"><span data-stu-id="d0ac6-122">Paste Counter List</span></span>
    -   <span data-ttu-id="d0ac6-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0ac6-123">Properties</span></span>

<span data-ttu-id="d0ac6-124">Tenga en cuenta que esta propiedad solo afecta a la capacidad del usuario de modificar los valores de propiedad a través de la interfaz de usuario, pero no le impide modificar mediante programación los valores o los contadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d0ac6-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ac6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ac6-125">Requirements</span></span>



| <span data-ttu-id="d0ac6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ac6-126">Requirement</span></span> | <span data-ttu-id="d0ac6-127">Value</span><span class="sxs-lookup"><span data-stu-id="d0ac6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ac6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ac6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ac6-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0ac6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d0ac6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ac6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ac6-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0ac6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0ac6-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0ac6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ac6-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac6-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ac6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0ac6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac6-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="d0ac6-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





