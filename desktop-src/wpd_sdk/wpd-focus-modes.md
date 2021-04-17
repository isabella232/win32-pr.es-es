---
description: El \_ tipo de enumeración de modos de enfoque de WPD \_ describe el modo de enfoque utilizado por un dispositivo de captura de imagen fija.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumeración WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671011"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="a060e-103">\_Enumeración de modos de enfoque de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a060e-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="a060e-104">El tipo de enumeración de **\_ \_ modos de enfoque de WPD** describe el modo de enfoque utilizado por un dispositivo de captura de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="a060e-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a060e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a060e-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="a060e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a060e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a060e-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**enfoque de WPD \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="a060e-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="a060e-108">No se ha especificado el modo de enfoque.</span><span class="sxs-lookup"><span data-stu-id="a060e-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="a060e-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_manual del foco de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a060e-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="a060e-110">Especifica el foco manual.</span><span class="sxs-lookup"><span data-stu-id="a060e-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="a060e-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_enfoque \_ automático de WPD**</span><span class="sxs-lookup"><span data-stu-id="a060e-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="a060e-112">Especifica el foco automático, controlado por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a060e-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="a060e-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automática de foco de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a060e-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="a060e-114">Especifica que el dispositivo debe cambiar automáticamente entre la macro y el foco normal, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a060e-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a060e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a060e-115">Remarks</span></span>

<span data-ttu-id="a060e-116">Esta enumeración se usa en la propiedad del modo de enfoque de imagen de la [ \_ \_ imagen \_ \_ de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a060e-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a060e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a060e-117">Requirements</span></span>



| <span data-ttu-id="a060e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a060e-118">Requirement</span></span> | <span data-ttu-id="a060e-119">Value</span><span class="sxs-lookup"><span data-stu-id="a060e-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a060e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a060e-120">Header</span></span><br/> | <dl> <span data-ttu-id="a060e-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a060e-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a060e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a060e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a060e-123">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="a060e-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




