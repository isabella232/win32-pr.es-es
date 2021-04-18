---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de información común.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propiedades de información común (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718893"
---
# <a name="common-information-properties"></a><span data-ttu-id="d9aad-103">Propiedades de información común</span><span class="sxs-lookup"><span data-stu-id="d9aad-103">Common Information Properties</span></span>

<span data-ttu-id="d9aad-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de información común.</span><span class="sxs-lookup"><span data-stu-id="d9aad-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="d9aad-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9aad-105">Property</span></span>                                      | <span data-ttu-id="d9aad-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d9aad-106">VarType</span></span>        | <span data-ttu-id="d9aad-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9aad-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aad-108">**\_notas de \_ información \_ común de WPD**</span><span class="sxs-lookup"><span data-stu-id="d9aad-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="d9aad-109">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="d9aad-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d9aad-110">En el caso de citas, tareas y objetos similares, esta propiedad contiene las notas del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d9aad-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="d9aad-111">**\_asunto de \_ información \_ común de WPD**</span><span class="sxs-lookup"><span data-stu-id="d9aad-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="d9aad-112">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="d9aad-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d9aad-113">Valor que especifica el campo de asunto de este objeto.</span><span class="sxs-lookup"><span data-stu-id="d9aad-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="d9aad-114">**\_ \_ \_ texto del cuerpo de información común de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d9aad-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="d9aad-115">**VT \_ LPWStr**</span><span class="sxs-lookup"><span data-stu-id="d9aad-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d9aad-116">Esta propiedad contiene el texto del cuerpo de un objeto, en formato de texto no cifrado o HTML.</span><span class="sxs-lookup"><span data-stu-id="d9aad-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="d9aad-117">**\_prioridad de \_ información \_ común de WPD**</span><span class="sxs-lookup"><span data-stu-id="d9aad-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="d9aad-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d9aad-118">**VT\_UI4**</span></span>    | <span data-ttu-id="d9aad-119">Valor que especifica la prioridad de este objeto.</span><span class="sxs-lookup"><span data-stu-id="d9aad-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="d9aad-120">0 indica la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="d9aad-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="d9aad-121">**\_ \_ \_ fecha y hora de inicio de información común de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d9aad-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="d9aad-122">**fecha de VT \_**</span><span class="sxs-lookup"><span data-stu-id="d9aad-122">**VT\_DATE**</span></span>   | <span data-ttu-id="d9aad-123">Valor que especifica la fecha y hora en que está programada la inicio de una cita, tarea u objeto similar.</span><span class="sxs-lookup"><span data-stu-id="d9aad-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="d9aad-124">**\_ \_ \_ fecha y hora de finalización de información común de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d9aad-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="d9aad-125">**fecha de VT \_**</span><span class="sxs-lookup"><span data-stu-id="d9aad-125">**VT\_DATE**</span></span>   | <span data-ttu-id="d9aad-126">Valor que especifica la fecha y hora en que está programada la finalización de una cita, tarea u objeto similar.</span><span class="sxs-lookup"><span data-stu-id="d9aad-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="d9aad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9aad-127">Requirements</span></span>



| <span data-ttu-id="d9aad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9aad-128">Requirement</span></span> | <span data-ttu-id="d9aad-129">Value</span><span class="sxs-lookup"><span data-stu-id="d9aad-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aad-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9aad-130">Header</span></span><br/> | <dl> <span data-ttu-id="d9aad-131"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9aad-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9aad-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9aad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9aad-133">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="d9aad-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




