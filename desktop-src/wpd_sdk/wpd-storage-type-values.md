---
description: El \_ tipo de \_ enumeración de valores de tipo de almacenamiento WPD \_ describe los distintos tipos de almacenamiento de dispositivos portátiles de Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumeración WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649867"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="5082b-103">\_ \_ Enumeración de valores de tipo de almacenamiento WPD \_</span><span class="sxs-lookup"><span data-stu-id="5082b-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="5082b-104">El tipo de enumeración de **\_ valores de \_ tipo \_ de almacenamiento WPD** describe los distintos tipos de almacenamiento de dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="5082b-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="5082b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5082b-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="5082b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5082b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5082b-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**tipo de almacenamiento de WPD sin \_ \_ \_ definir**</span><span class="sxs-lookup"><span data-stu-id="5082b-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5082b-108">El almacenamiento es de un tipo no definido.</span><span class="sxs-lookup"><span data-stu-id="5082b-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5082b-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**tipo de almacenamiento WPD de \_ \_ \_ \_ ROM fijo**</span><span class="sxs-lookup"><span data-stu-id="5082b-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="5082b-110">El almacenamiento no es extraíble y de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5082b-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="5082b-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ ROM extraíble del tipo de almacenamiento de \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5082b-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="5082b-112">El almacenamiento es extraíble y es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5082b-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="5082b-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ \_ memoria RAM fija de tipo de almacenamiento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5082b-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="5082b-114">El almacenamiento no es extraíble y es compatible con lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5082b-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="5082b-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ memoria RAM extraíble del tipo de almacenamiento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5082b-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="5082b-116">El almacenamiento es extraíble y es compatible con lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5082b-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5082b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5082b-117">Remarks</span></span>

<span data-ttu-id="5082b-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5082b-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5082b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5082b-119">Requirements</span></span>



| <span data-ttu-id="5082b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5082b-120">Requirement</span></span> | <span data-ttu-id="5082b-121">Value</span><span class="sxs-lookup"><span data-stu-id="5082b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5082b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5082b-122">Header</span></span><br/> | <dl> <span data-ttu-id="5082b-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5082b-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5082b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5082b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5082b-125">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="5082b-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




