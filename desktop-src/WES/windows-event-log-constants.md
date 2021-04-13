---
title: Constantes del registro de eventos de Windows (WinEvt. h)
description: 'El registro de eventos de Windows define las constantes siguientes:'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422290"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="a6317-103">Constantes del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="a6317-103">Windows Event Log Constants</span></span>

<span data-ttu-id="a6317-104">El registro de eventos de Windows define las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6317-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="a6317-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT \_ variante \_ Type \_ Mask**</span><span class="sxs-lookup"><span data-stu-id="a6317-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="a6317-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="a6317-107">Máscara de bits que se usa para enmascarar el bit de la matriz del tipo variante, de modo que pueda determinar el tipo de datos del valor Variant que contiene la estructura de la [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .</span><span class="sxs-lookup"><span data-stu-id="a6317-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6317-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT \_ variante \_ Type \_ array**</span><span class="sxs-lookup"><span data-stu-id="a6317-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-109">128</span><span class="sxs-lookup"><span data-stu-id="a6317-109">128</span></span>
</dt> <dt>



<span data-ttu-id="a6317-110">El miembro de **tipo** de la estructura [**evt \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) tiene este bit establecido si la variante contiene un puntero a una matriz de valores, en lugar del propio valor.</span><span class="sxs-lookup"><span data-stu-id="a6317-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6317-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT \_ - \_ acceso de lectura**</span><span class="sxs-lookup"><span data-stu-id="a6317-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-112">0x1</span><span class="sxs-lookup"><span data-stu-id="a6317-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="a6317-113">Permiso de control de acceso de lectura que permite leer información de un registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="a6317-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6317-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_acceso de escritura de EVT \_**</span><span class="sxs-lookup"><span data-stu-id="a6317-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-115">0x2</span><span class="sxs-lookup"><span data-stu-id="a6317-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="a6317-116">Permiso de control de acceso de escritura que permite escribir información en un registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="a6317-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6317-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT \_ - \_ acceso sin formato**</span><span class="sxs-lookup"><span data-stu-id="a6317-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-118">0x4</span><span class="sxs-lookup"><span data-stu-id="a6317-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="a6317-119">Permiso Clear Access Control que permite borrar toda la información de un registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="a6317-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a6317-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ All \_ Access**</span><span class="sxs-lookup"><span data-stu-id="a6317-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6317-121">0X7</span><span class="sxs-lookup"><span data-stu-id="a6317-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="a6317-122">Todos los permisos de control de acceso (lectura, escritura, borrado y eliminación).</span><span class="sxs-lookup"><span data-stu-id="a6317-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6317-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6317-123">Requirements</span></span>



| <span data-ttu-id="a6317-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6317-124">Requirement</span></span> | <span data-ttu-id="a6317-125">Value</span><span class="sxs-lookup"><span data-stu-id="a6317-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6317-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6317-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a6317-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6317-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a6317-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6317-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a6317-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6317-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a6317-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6317-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6317-131"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6317-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





