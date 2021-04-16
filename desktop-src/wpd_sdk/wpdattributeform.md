---
description: El tipo de enumeración WpdAttributeForm describe el modo en que una propiedad almacena sus valores.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumeración WpdAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650187"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="7fcfc-103">Enumeración WpdAttributeForm</span><span class="sxs-lookup"><span data-stu-id="7fcfc-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="7fcfc-104">El tipo de enumeración **WpdAttributeForm** describe el modo en que una propiedad almacena sus valores.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcfc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fcfc-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="7fcfc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7fcfc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7fcfc-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**formulario de atributo de propiedad de WPD no \_ \_ \_ \_ especificado**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="7fcfc-108">No se especifica el formato de los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="7fcfc-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_rango de \_ formulario de atributos de propiedad de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="7fcfc-110">El valor se expresa como un intervalo de valores, con un mínimo y un máximo.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="7fcfc-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ enumeración de formulario de atributo de propiedad de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="7fcfc-112">La propiedad tiene una serie de valores individuales.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="7fcfc-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expresión regular del formulario de atributo \_ de propiedad de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="7fcfc-114">El valor de propiedad es una expresión regular, no una expresión literal.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="7fcfc-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_ \_ \_ identificador OJBECT del formulario de atributo \_ de propiedad de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="7fcfc-116">El valor de propiedad representa un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="7fcfc-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fcfc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fcfc-117">Remarks</span></span>

<span data-ttu-id="7fcfc-118">Esta enumeración la usa la propiedad del formulario de atributo de propiedad de WPD para describir cómo se almacenan los datos de una propiedad. [ \_ \_ \_ ](attributes.md)</span><span class="sxs-lookup"><span data-stu-id="7fcfc-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcfc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fcfc-119">Requirements</span></span>



| <span data-ttu-id="7fcfc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fcfc-120">Requirement</span></span> | <span data-ttu-id="7fcfc-121">Value</span><span class="sxs-lookup"><span data-stu-id="7fcfc-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcfc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fcfc-122">Header</span></span><br/> | <dl> <span data-ttu-id="7fcfc-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfc-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcfc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fcfc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcfc-125">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="7fcfc-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




