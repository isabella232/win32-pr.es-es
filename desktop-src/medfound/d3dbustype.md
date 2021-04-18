---
description: Especifica el tipo de bus de e/s utilizado por el adaptador de gráficos.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumeración D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714921"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="ab796-103">Enumeración D3DBUSTYPE</span><span class="sxs-lookup"><span data-stu-id="ab796-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="ab796-104">Especifica el tipo de bus de e/s utilizado por el adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ab796-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab796-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab796-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="ab796-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ab796-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab796-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ otro**</span><span class="sxs-lookup"><span data-stu-id="ab796-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-108">Indica un tipo de bus distinto de los tipos que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="ab796-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**\_PCI D3DBUSTYPE**</span><span class="sxs-lookup"><span data-stu-id="ab796-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-110">Bus PCI.</span><span class="sxs-lookup"><span data-stu-id="ab796-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**</span><span class="sxs-lookup"><span data-stu-id="ab796-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-112">Bus PCI-X.</span><span class="sxs-lookup"><span data-stu-id="ab796-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**</span><span class="sxs-lookup"><span data-stu-id="ab796-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-114">Bus PCI Express.</span><span class="sxs-lookup"><span data-stu-id="ab796-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="ab796-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-116">Bus del puerto de gráficos acelerado (AGP).</span><span class="sxs-lookup"><span data-stu-id="ab796-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL \_ modificador \_ dentro \_ del \_ chipset**</span><span class="sxs-lookup"><span data-stu-id="ab796-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-118">La implementación del adaptador de gráficos está en el puente norte del chipset de la placa base.</span><span class="sxs-lookup"><span data-stu-id="ab796-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="ab796-119">Esta marca implica que los datos nunca atraviesan un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ab796-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL el \_ modificador \_ realiza un seguimiento \_ de la \_ placa madre en \_ \_ \_ chip**</span><span class="sxs-lookup"><span data-stu-id="ab796-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-121">Indica que el adaptador de gráficos está conectado al puente norte del chipset de la placa base mediante el seguimiento de la placa base y que todos los chips del adaptador gráfico están soldados a la placa base.</span><span class="sxs-lookup"><span data-stu-id="ab796-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="ab796-122">Esta marca implica que los datos nunca atraviesan un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ab796-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL el \_ modificador \_ realiza un seguimiento \_ de la \_ placa madre \_ \_ \_ en el socket**</span><span class="sxs-lookup"><span data-stu-id="ab796-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-124">El adaptador de gráficos se conecta al puente norte del chipset de la placa base siguiendo las pistas de la placa base, y todos los chips del adaptador de gráficos se conectan a través de sockets a la placa base.</span><span class="sxs-lookup"><span data-stu-id="ab796-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Conector de la \_ \_ placa secundaria del modificador D3DBUSIMPL \_**</span><span class="sxs-lookup"><span data-stu-id="ab796-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-126">El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard.</span><span class="sxs-lookup"><span data-stu-id="ab796-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ Conector de la placa secundaria del modificador D3DBUSIMPL \_ \_ \_ dentro \_ de \_ NUAE**</span><span class="sxs-lookup"><span data-stu-id="ab796-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-128">El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard y el adaptador de gráficos está dentro de un contenedor que no es accesible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ab796-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="ab796-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificador D3DBUSIMPL \_ no \_ estándar**</span><span class="sxs-lookup"><span data-stu-id="ab796-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="ab796-130">Se establece una de las marcas de modificador XXX del modificador D3DBUSIMPL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab796-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab796-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab796-131">Remarks</span></span>

<span data-ttu-id="ab796-132">Se pueden establecer tres marcas como máximo.</span><span class="sxs-lookup"><span data-stu-id="ab796-132">As many as three flags can be set.</span></span> <span data-ttu-id="ab796-133">Las marcas en el intervalo de 0x00 a 0x04 (**D3DBUSTYPE \_ XXX**) proporcionan el tipo de bus básico.</span><span class="sxs-lookup"><span data-stu-id="ab796-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="ab796-134">Las marcas en el intervalo de 0x10000 a 0x50000 (**D3DBUSIMPL \_ modificador \_ XXX**) modifican la descripción básica.</span><span class="sxs-lookup"><span data-stu-id="ab796-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="ab796-135">El controlador establece una marca de tipo bus y puede establecer cero o un marcador de modificador.</span><span class="sxs-lookup"><span data-stu-id="ab796-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="ab796-136">Si el controlador establece una marca de modificador, también establece la marca del **\_ modificador D3DBUSIMPL \_ no \_ estándar** .</span><span class="sxs-lookup"><span data-stu-id="ab796-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="ab796-137">Las marcas se combinan con una **operación OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="ab796-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab796-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab796-138">Requirements</span></span>



| <span data-ttu-id="ab796-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab796-139">Requirement</span></span> | <span data-ttu-id="ab796-140">Value</span><span class="sxs-lookup"><span data-stu-id="ab796-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab796-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab796-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ab796-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab796-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab796-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab796-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ab796-144">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab796-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ab796-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab796-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab796-146"><dt>D3d9types. h (incluye d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab796-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab796-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab796-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab796-148">Enumeraciones de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ab796-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




