---
title: Estructura de WMDM_PROP_DESC
description: La \_ estructura de \_ Descripción de la propiedad WMDM describe los valores válidos de una propiedad en una configuración de propiedades determinada.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Estructura WMDM_PROP_DESC Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700176"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="95212-104">Estructura de descripción de la \_ propiedades WMDM \_</span><span class="sxs-lookup"><span data-stu-id="95212-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="95212-105">La estructura de **\_ \_ Descripción** de la propiedad WMDM describe los valores válidos de una propiedad en una configuración de propiedades determinada.</span><span class="sxs-lookup"><span data-stu-id="95212-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="95212-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95212-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="95212-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95212-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="95212-108">**pwszPropName**</span><span class="sxs-lookup"><span data-stu-id="95212-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="95212-109">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="95212-109">Name of the property.</span></span> <span data-ttu-id="95212-110">La aplicación debe liberar esta memoria cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="95212-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="95212-111">**ValidValuesForm**</span><span class="sxs-lookup"><span data-stu-id="95212-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="95212-112">Un valor de enumeración de [**\_ \_ \_ \_ \_ formulario de valores válidos prop enum de WMDM**](wmdm-enum-prop-valid-values-form.md) que describe el tipo de valores, como un intervalo o una lista.</span><span class="sxs-lookup"><span data-stu-id="95212-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="95212-113">El valor de esta enumeración determina qué variable miembro se utiliza.</span><span class="sxs-lookup"><span data-stu-id="95212-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="95212-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="95212-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="95212-115">Contiene los valores válidos de la propiedad en una configuración de propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="95212-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="95212-116">Este miembro contiene uno de tres elementos: el valor de enumeración WMDM \_ Enumerate \_ \_ valores válidos \_ \_ Any; el miembro **ValidValuesRange**; o el miembro **EnumeratedValidValues**.</span><span class="sxs-lookup"><span data-stu-id="95212-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="95212-117">El valor o el miembro está indicado por **ValidValuesForm**.</span><span class="sxs-lookup"><span data-stu-id="95212-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="95212-118">**ValidValuesRange**</span><span class="sxs-lookup"><span data-stu-id="95212-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="95212-119">Una estructura de intervalo de valores de propiedades de WMDM que contiene un intervalo de valores válidos. [**\_ \_ \_**](wmdm-prop-values-range.md)</span><span class="sxs-lookup"><span data-stu-id="95212-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="95212-120">Solo está presente cuando **ValidValuesForm** se establece en la enumeración de WMDM de \_ \_ \_ valores válidos \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="95212-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="95212-121">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="95212-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="95212-122">**EnumeratedValidValues**</span><span class="sxs-lookup"><span data-stu-id="95212-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="95212-123">Estructura [**de \_ \_ \_ enumeración de valores de propiedades de WMDM**](wmdm-prop-values-enum.md) que contiene un conjunto enumerado de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="95212-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="95212-124">Esto solo está presente cuando **ValidValuesForm** se establece en la \_ enumeración de WMDM de \_ \_ valores válidos de enum \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="95212-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="95212-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="95212-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95212-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95212-126">Remarks</span></span>

<span data-ttu-id="95212-127">La estructura de descripción de la propiedad **WMDM \_ \_** contiene una descripción de propiedad formada por un nombre de propiedad y sus valores válidos en una configuración determinada.</span><span class="sxs-lookup"><span data-stu-id="95212-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="95212-128">El llamador debe liberar la memoria usada por **ValidValuesRange** o **EnumeratedValues**.</span><span class="sxs-lookup"><span data-stu-id="95212-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="95212-129">Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="95212-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95212-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95212-130">Requirements</span></span>



| <span data-ttu-id="95212-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="95212-131">Requirement</span></span> | <span data-ttu-id="95212-132">Value</span><span class="sxs-lookup"><span data-stu-id="95212-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="95212-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95212-133">Header</span></span><br/> | <dl> <span data-ttu-id="95212-134"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95212-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95212-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="95212-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95212-136">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="95212-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="95212-137">**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="95212-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="95212-138">**\_funcionalidad de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="95212-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="95212-139">**\_configuración de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="95212-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="95212-140">**\_ \_ enumeración de valores de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="95212-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="95212-141">**\_intervalo de \_ valores de prop de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="95212-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="95212-142">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="95212-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





