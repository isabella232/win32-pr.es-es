---
title: Estructura de WMDM_FORMAT_CAPABILITY
description: La \_ \_ estructura de la funcionalidad de formato WMDM describe las capacidades de un dispositivo para un formato determinado.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- Estructura WMDM_FORMAT_CAPABILITY Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698695"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="aa0e9-104">Estructura de la \_ funcionalidad de formato WMDM \_</span><span class="sxs-lookup"><span data-stu-id="aa0e9-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="aa0e9-105">La estructura de la **\_ \_ funcionalidad de formato WMDM** describe las capacidades de un dispositivo para un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="aa0e9-106">Esta estructura contiene un conjunto de configuraciones de propiedades en una matriz de estructuras de **\_ \_ configuración de propiedades de WMDM** .</span><span class="sxs-lookup"><span data-stu-id="aa0e9-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="aa0e9-107">Cada configuración de propiedad representa un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="aa0e9-108">La aplicación puede obtener esta estructura llamando al método **IWMDMDevice3:: GetFormatCapability** y pasando el código de formato.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="aa0e9-109">Para obtener una lista de códigos de formato, consulte [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e9-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0e9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa0e9-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="aa0e9-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa0e9-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa0e9-112">**nPropConfig**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="aa0e9-113">Número de configuraciones de propiedades en la matriz **pConfigs** .</span><span class="sxs-lookup"><span data-stu-id="aa0e9-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="aa0e9-114">**pConfigs**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="aa0e9-115">Puntero a una matriz de estructuras de [**\_ \_ configuración de propiedades de WMDM**](wmdm-prop-config.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0e9-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="aa0e9-116">El tamaño de la matriz es igual al valor de **nPropConfig**.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa0e9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa0e9-117">Remarks</span></span>

<span data-ttu-id="aa0e9-118">La estructura de **\_ \_ capacidad del formato WMDM** proporciona un mecanismo flexible para expresar las capacidades del dispositivo para un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="aa0e9-119">Si el contenido está pensado para que lo represente el dispositivo (por ejemplo, un archivo de audio que va a reproducir el dispositivo), las propiedades del contenido deben coincidir con una de las configuraciones de propiedades devueltas por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) en la estructura de la **\_ \_ capacidad del formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="aa0e9-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="aa0e9-120">Por ejemplo, para un archivo de audio, la velocidad de bits y la velocidad de muestreo deben cumplir una de las configuraciones de propiedades devueltas.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="aa0e9-121">El autor de la llamada es responsable de liberar la memoria asignada para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="aa0e9-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="aa0e9-122">La siguiente función muestra cómo borrar una estructura **de \_ \_ capacidad de formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="aa0e9-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="aa0e9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa0e9-123">Requirements</span></span>



| <span data-ttu-id="aa0e9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0e9-124">Requirement</span></span> | <span data-ttu-id="aa0e9-125">Value</span><span class="sxs-lookup"><span data-stu-id="aa0e9-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0e9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa0e9-126">Header</span></span><br/> | <dl> <span data-ttu-id="aa0e9-127"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa0e9-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0e9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa0e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0e9-129">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="aa0e9-130">**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="aa0e9-131">**\_configuración de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="aa0e9-132">**Descripción de la Prop de WMDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="aa0e9-133">**\_ \_ enumeración de valores de propiedades de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="aa0e9-134">**\_intervalo de \_ valores de prop de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="aa0e9-135">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="aa0e9-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





