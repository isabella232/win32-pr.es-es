---
title: Estructura de WMDM_PROP_VALUES_ENUM
description: La \_ \_ \_ estructura de enumeración valores de prop de WMDM contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Estructura WMDM_PROP_VALUES_ENUM Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698738"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="d50aa-104">\_Estructura de \_ enumeración de valores de propiedades de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="d50aa-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="d50aa-105">La estructura de **\_ \_ \_ enumeración valores de prop de WMDM** contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="d50aa-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50aa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d50aa-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="d50aa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d50aa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d50aa-108">**cEnumValues**</span><span class="sxs-lookup"><span data-stu-id="d50aa-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="d50aa-109">Recuento de valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="d50aa-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="d50aa-110">**pValues**</span><span class="sxs-lookup"><span data-stu-id="d50aa-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="d50aa-111">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="d50aa-111">Pointer to an array of values.</span></span> <span data-ttu-id="d50aa-112">El tamaño de la matriz es igual al valor de **cEnumValues**.</span><span class="sxs-lookup"><span data-stu-id="d50aa-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d50aa-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d50aa-113">Remarks</span></span>

<span data-ttu-id="d50aa-114">Esta estructura se usa en la estructura de **\_ \_ Descripción** de la propiedades de WMDM para describir un conjunto enumerado de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="d50aa-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="d50aa-115">Se puede aplicar un conjunto enumerado de valores válidos si se selecciona la enumeración de la enumeración de valores válidos \_ \_ prop enum de WMDM \_ \_ \_ en la enumeración del **\_ \_ \_ \_ \_ formulario de valores válidos** de la enumeración WMDM.</span><span class="sxs-lookup"><span data-stu-id="d50aa-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="d50aa-116">El llamador debe liberar la memoria usada por **pValues**.</span><span class="sxs-lookup"><span data-stu-id="d50aa-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="d50aa-117">Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="d50aa-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d50aa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d50aa-118">Requirements</span></span>



| <span data-ttu-id="d50aa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50aa-119">Requirement</span></span> | <span data-ttu-id="d50aa-120">Value</span><span class="sxs-lookup"><span data-stu-id="d50aa-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d50aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d50aa-121">Header</span></span><br/> | <dl> <span data-ttu-id="d50aa-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d50aa-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d50aa-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d50aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50aa-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="d50aa-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="d50aa-125">**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="d50aa-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="d50aa-126">**\_funcionalidad de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d50aa-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="d50aa-127">**\_configuración de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d50aa-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="d50aa-128">**Descripción de la Prop de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d50aa-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="d50aa-129">**\_intervalo de \_ valores de prop de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d50aa-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="d50aa-130">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="d50aa-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





