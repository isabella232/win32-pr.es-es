---
description: Describe cómo un parámetro (método o evento) almacena su valor.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumeración WpdParameterAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649603"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="c3ac2-103">Enumeración WpdParameterAttributeForm</span><span class="sxs-lookup"><span data-stu-id="c3ac2-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="c3ac2-104">El tipo de enumeración [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) describe cómo un parámetro (método o evento) almacena su valor.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ac2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3ac2-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="c3ac2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c3ac2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c3ac2-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**formulario de atributo de parámetro WPD no \_ \_ \_ \_ especificado**</span><span class="sxs-lookup"><span data-stu-id="c3ac2-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="c3ac2-108">No se ha especificado el formato del parámetro.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac2-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_rango de \_ formulario de atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3ac2-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="c3ac2-110">El parámetro especifica un intervalo.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac2-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ enumeración de formulario de atributo de parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c3ac2-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="c3ac2-112">El parámetro es una enumeración.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac2-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ expresión regular del formulario de atributo \_ de parámetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c3ac2-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="c3ac2-114">El parámetro es una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="c3ac2-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_identificador de \_ objeto de atributo de parámetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3ac2-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="c3ac2-116">El parámetro es un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="c3ac2-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3ac2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ac2-117">Requirements</span></span>



| <span data-ttu-id="c3ac2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ac2-118">Requirement</span></span> | <span data-ttu-id="c3ac2-119">Value</span><span class="sxs-lookup"><span data-stu-id="c3ac2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ac2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3ac2-120">Header</span></span><br/> | <dl> <span data-ttu-id="c3ac2-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ac2-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

