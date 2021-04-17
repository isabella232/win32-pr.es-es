---
title: Estructura de WMDM_PROP_VALUES_RANGE
description: La \_ \_ \_ estructura de intervalo de valores de prop de WMDM describe un intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Estructura WMDM_PROP_VALUES_RANGE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698737"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="5b5f7-104">\_Estructura de \_ intervalo de valores de prop de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="5b5f7-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="5b5f7-105">La estructura de intervalo de valores de prop de WMDM describe un intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b5f7-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="5b5f7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b5f7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b5f7-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="5b5f7-109">Valor mínimo del intervalo.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="5b5f7-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="5b5f7-111">Valor máximo del intervalo.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="5b5f7-112">**rangeStep**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="5b5f7-113">Tamaño del paso en el que los valores válidos aumentan desde el valor mínimo hasta el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="5b5f7-114">Esto permite especificar valores permitidos discretos en un intervalo.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b5f7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b5f7-115">Remarks</span></span>

<span data-ttu-id="5b5f7-116">Esta estructura se usa en la estructura de [**\_ \_ Descripción**](wmdm-prop-desc.md) de la props de WMDM para describir un intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5b5f7-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="5b5f7-117">Un intervalo de valores válidos es aplicable cuando \_ \_ se selecciona la enumeración de valores válidos prop enum de WMDM \_ \_ \_ en la enumeración de WMDM enumeración de valores [**\_ \_ \_ válidos \_ \_ prop**](wmdm-enum-prop-valid-values-form.md) .</span><span class="sxs-lookup"><span data-stu-id="5b5f7-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5f7-118">Requirements</span></span>



| <span data-ttu-id="5b5f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5f7-119">Requirement</span></span> | <span data-ttu-id="5b5f7-120">Value</span><span class="sxs-lookup"><span data-stu-id="5b5f7-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5f7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b5f7-121">Header</span></span><br/> | <dl> <span data-ttu-id="5b5f7-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b5f7-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5f7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b5f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5f7-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="5b5f7-125">**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="5b5f7-126">**\_funcionalidad de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="5b5f7-127">**\_configuración de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="5b5f7-128">**Descripción de la Prop de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="5b5f7-129">**\_ \_ enumeración de valores de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="5b5f7-130">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="5b5f7-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





