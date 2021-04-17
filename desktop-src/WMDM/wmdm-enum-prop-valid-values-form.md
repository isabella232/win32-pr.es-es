---
title: Enumeración WMDM_ENUM_PROP_VALID_VALUES_FORM
description: El \_ \_ \_ \_ \_ tipo de enumeración de formulario de valores válidos prop enum de WMDM describe posibles formas de valores válidos para una propiedad.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Enumeración WMDM_ENUM_PROP_VALID_VALUES_FORM Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698618"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="61d32-104">\_ \_ \_ \_ Enumeración del formulario de valores válidos prop enum de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="61d32-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="61d32-105">El tipo de enumeración de **\_ \_ \_ \_ \_ formulario de valores válidos prop enum de WMDM** describe posibles formas de valores válidos para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="61d32-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d32-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61d32-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="61d32-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="61d32-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61d32-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**\_ \_ \_ valores válidos de \_ la enumeración WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="61d32-109">Todos los valores son válidos.</span><span class="sxs-lookup"><span data-stu-id="61d32-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="61d32-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_intervalo de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="61d32-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="61d32-111">Los valores válidos se expresan como un intervalo.</span><span class="sxs-lookup"><span data-stu-id="61d32-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="61d32-112">Para obtener información detallada, consulte la estructura de [**intervalo de valores de propiedades de WMDM \_ \_ \_**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="61d32-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="61d32-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**enumeración de \_ \_ \_ valores válidos prop \_ \_ enum de WMDM**</span><span class="sxs-lookup"><span data-stu-id="61d32-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="61d32-114">Los valores válidos son un conjunto enumerado.</span><span class="sxs-lookup"><span data-stu-id="61d32-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="61d32-115">Para obtener información detallada, consulte la estructura de [**\_ \_ \_ enumeración de valores de propiedades de WMDM**](wmdm-prop-values-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="61d32-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61d32-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61d32-116">Remarks</span></span>

<span data-ttu-id="61d32-117">Esta enumeración se usa en la estructura de [**\_ \_ Descripción**](wmdm-prop-desc.md) de la propiedad WMDM para especificar el formato de los valores válidos de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="61d32-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61d32-118">Requirements</span></span>



| <span data-ttu-id="61d32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="61d32-119">Requirement</span></span> | <span data-ttu-id="61d32-120">Value</span><span class="sxs-lookup"><span data-stu-id="61d32-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61d32-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61d32-121">Header</span></span><br/> | <dl> <span data-ttu-id="61d32-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61d32-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61d32-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="61d32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d32-124">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="61d32-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="61d32-125">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="61d32-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="61d32-126">**\_funcionalidad de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="61d32-127">**\_configuración de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="61d32-128">**Descripción de la Prop de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="61d32-129">**\_ \_ enumeración de valores de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="61d32-130">**\_intervalo de \_ valores de prop de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="61d32-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





