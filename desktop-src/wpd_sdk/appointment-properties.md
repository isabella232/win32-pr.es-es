---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de cita.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Propiedades de la cita (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700142"
---
# <a name="appointment-properties"></a><span data-ttu-id="55cfa-103">Propiedades de cita</span><span class="sxs-lookup"><span data-stu-id="55cfa-103">Appointment Properties</span></span>

<span data-ttu-id="55cfa-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="55cfa-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55cfa-105">Property</span></span>                                   | <span data-ttu-id="55cfa-106">VarType</span><span class="sxs-lookup"><span data-stu-id="55cfa-106">VarType</span></span>        | <span data-ttu-id="55cfa-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="55cfa-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55cfa-108">**\_ \_ asistentes aceptados por la cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="55cfa-109">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-110">Lista delimitada por signos de punto y coma de los asistentes que han aceptado la cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="55cfa-111">**\_ \_ Asistente rechazado de citas de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="55cfa-112">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-113">Lista delimitada por signos de punto y coma de los asistentes que han rechazado la cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="55cfa-114">**\_Ubicación de citas de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="55cfa-115">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="55cfa-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="55cfa-116">Una ubicación fácil de lectura de la cita, por ejemplo, "Building 5, Room 7".</span><span class="sxs-lookup"><span data-stu-id="55cfa-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="55cfa-117">**\_ \_ asistentes opcionales de cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="55cfa-118">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-119">Lista delimitada por signos de punto y coma de asistentes opcionales para la cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="55cfa-120">**\_ \_ asistentes requeridos de la cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="55cfa-121">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-122">Lista delimitada por signos de punto y coma de los asistentes necesarios para la cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="55cfa-123">**\_recursos de cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="55cfa-124">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-125">Lista delimitada por signos de punto y coma de los recursos necesarios para la cita.</span><span class="sxs-lookup"><span data-stu-id="55cfa-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="55cfa-126">**\_ \_ asistentes provisionales de cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="55cfa-127">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-128">Lista delimitada por signos de punto y coma de los asistentes que han aceptado la cita provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="55cfa-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="55cfa-129">**\_tipo de cita de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="55cfa-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="55cfa-130">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="55cfa-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="55cfa-131">El tipo de cita, por ejemplo, "personal", "Business", etc.</span><span class="sxs-lookup"><span data-stu-id="55cfa-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="55cfa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55cfa-132">Requirements</span></span>



| <span data-ttu-id="55cfa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="55cfa-133">Requirement</span></span> | <span data-ttu-id="55cfa-134">Value</span><span class="sxs-lookup"><span data-stu-id="55cfa-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cfa-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55cfa-135">Header</span></span><br/> | <dl> <span data-ttu-id="55cfa-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="55cfa-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55cfa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="55cfa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cfa-138">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="55cfa-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




