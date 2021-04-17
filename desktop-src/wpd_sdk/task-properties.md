---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de tarea.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propiedades de la tarea (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708670"
---
# <a name="task-properties"></a><span data-ttu-id="9af02-103">Propiedades de la tarea</span><span class="sxs-lookup"><span data-stu-id="9af02-103">Task Properties</span></span>

<span data-ttu-id="9af02-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de tarea.</span><span class="sxs-lookup"><span data-stu-id="9af02-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="9af02-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9af02-105">Property</span></span>                         | <span data-ttu-id="9af02-106">VarType</span><span class="sxs-lookup"><span data-stu-id="9af02-106">VarType</span></span>        | <span data-ttu-id="9af02-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9af02-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af02-108">**propietario de la tarea de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9af02-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="9af02-109">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="9af02-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9af02-110">Propietario de la tarea.</span><span class="sxs-lookup"><span data-stu-id="9af02-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="9af02-111">**\_ \_ porcentaje \_ completado de la tarea de WPD**</span><span class="sxs-lookup"><span data-stu-id="9af02-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="9af02-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9af02-112">**VT\_UI4**</span></span>    | <span data-ttu-id="9af02-113">Un número entre 0 y 100 que especifica cómo se completa la tarea.</span><span class="sxs-lookup"><span data-stu-id="9af02-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="9af02-114">**\_fecha de \_ recordatorio de tarea de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9af02-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="9af02-115">**fecha de VT \_**</span><span class="sxs-lookup"><span data-stu-id="9af02-115">**VT\_DATE**</span></span>   | <span data-ttu-id="9af02-116">Valor que especifica cuándo se debe enviar un recordatorio para realizar la tarea, si no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9af02-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="9af02-117">**Estado de la tarea de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9af02-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="9af02-118">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="9af02-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9af02-119">Una descripción de cadena del estado de la tarea, por ejemplo, "en curso".</span><span class="sxs-lookup"><span data-stu-id="9af02-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="9af02-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af02-120">Requirements</span></span>



| <span data-ttu-id="9af02-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af02-121">Requirement</span></span> | <span data-ttu-id="9af02-122">Value</span><span class="sxs-lookup"><span data-stu-id="9af02-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af02-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9af02-123">Header</span></span><br/> | <dl> <span data-ttu-id="9af02-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af02-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af02-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af02-126">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="9af02-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




