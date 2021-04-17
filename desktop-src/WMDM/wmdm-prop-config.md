---
title: Estructura de WMDM_PROP_CONFIG
description: La \_ \_ estructura de configuración de propiedades de WMDM describe un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con el dispositivo para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras de propiedades DESC de WMDM \_ \_ .
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Estructura WMDM_PROP_CONFIG Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698531"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="dc589-105">Estructura de configuración de \_ propiedades de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="dc589-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="dc589-106">La estructura de **\_ \_ configuración de propiedades de WMDM** describe un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con el dispositivo para un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="dc589-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="dc589-107">Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras de propiedades [**\_ \_ DESC de WMDM**](wmdm-prop-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="dc589-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc589-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc589-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="dc589-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc589-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc589-110">**nPreference**</span><span class="sxs-lookup"><span data-stu-id="dc589-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="dc589-111">Nivel de preferencia del dispositivo para esta configuración.</span><span class="sxs-lookup"><span data-stu-id="dc589-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="dc589-112">El valor más bajo indica la configuración preferida.</span><span class="sxs-lookup"><span data-stu-id="dc589-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dc589-113">**nPropDesc**</span><span class="sxs-lookup"><span data-stu-id="dc589-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="dc589-114">Número de descripciones de propiedad contenidas en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="dc589-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="dc589-115">Hay una única descripción de propiedad para cada propiedad admitida para el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="dc589-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="dc589-116">**pPropDesc**</span><span class="sxs-lookup"><span data-stu-id="dc589-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="dc589-117">Puntero a una matriz de estructuras de tipo [**\_ \_ DESC de WMDM**](wmdm-prop-desc.md) que contienen descripciones de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc589-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="dc589-118">El tamaño de la matriz es igual al valor de **nPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="dc589-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="dc589-119">La aplicación debe liberar esta memoria cuando termine.</span><span class="sxs-lookup"><span data-stu-id="dc589-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc589-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc589-120">Remarks</span></span>

<span data-ttu-id="dc589-121">La estructura de la [**\_ \_ capacidad del formato WMDM**](wmdm-format-capability.md) devuelta por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) para un formato determinado consta de varias configuraciones de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc589-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="dc589-122">**WMDM \_ Las \_** estructuras de configuración de prop describen esas configuraciones.</span><span class="sxs-lookup"><span data-stu-id="dc589-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="dc589-123">Una configuración de propiedades describe los valores de todas las propiedades compatibles con un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="dc589-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="dc589-124">Los valores de propiedades diferentes en una sola configuración son compatibles entre sí.</span><span class="sxs-lookup"><span data-stu-id="dc589-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="dc589-125">Por ejemplo, para un archivo de audio, una configuración incluirá valores válidos de la velocidad de muestra y valores válidos de la velocidad de bits, de modo que todas las combinaciones de estas velocidades de ejemplo y de bits se puedan reproducir en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc589-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="dc589-126">El llamador debe liberar la memoria usada por **pPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="dc589-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="dc589-127">Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="dc589-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc589-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc589-128">Requirements</span></span>



| <span data-ttu-id="dc589-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc589-129">Requirement</span></span> | <span data-ttu-id="dc589-130">Value</span><span class="sxs-lookup"><span data-stu-id="dc589-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc589-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc589-131">Header</span></span><br/> | <dl> <span data-ttu-id="dc589-132"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc589-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc589-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc589-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc589-134">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="dc589-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="dc589-135">**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="dc589-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="dc589-136">**\_funcionalidad de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="dc589-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="dc589-137">**Descripción de la Prop de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dc589-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="dc589-138">**\_ \_ enumeración de valores de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="dc589-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="dc589-139">**\_intervalo de \_ valores de prop de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="dc589-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="dc589-140">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="dc589-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





