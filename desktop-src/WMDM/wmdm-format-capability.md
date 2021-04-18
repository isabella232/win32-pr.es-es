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
# <a name="wmdm_format_capability-structure"></a>Estructura de la \_ funcionalidad de formato WMDM \_

La estructura de la **\_ \_ funcionalidad de formato WMDM** describe las capacidades de un dispositivo para un formato determinado. Esta estructura contiene un conjunto de configuraciones de propiedades en una matriz de estructuras de **\_ \_ configuración de propiedades de WMDM** . Cada configuración de propiedad representa un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con un formato determinado. La aplicación puede obtener esta estructura llamando al método **IWMDMDevice3:: GetFormatCapability** y pasando el código de formato. Para obtener una lista de códigos de formato, consulte [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nPropConfig**
</dt> <dd>

Número de configuraciones de propiedades en la matriz **pConfigs** .

</dd> <dt>

**pConfigs**
</dt> <dd>

Puntero a una matriz de estructuras de [**\_ \_ configuración de propiedades de WMDM**](wmdm-prop-config.md) . El tamaño de la matriz es igual al valor de **nPropConfig**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ capacidad del formato WMDM** proporciona un mecanismo flexible para expresar las capacidades del dispositivo para un formato determinado.

Si el contenido está pensado para que lo represente el dispositivo (por ejemplo, un archivo de audio que va a reproducir el dispositivo), las propiedades del contenido deben coincidir con una de las configuraciones de propiedades devueltas por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) en la estructura de la **\_ \_ capacidad del formato WMDM** . Por ejemplo, para un archivo de audio, la velocidad de bits y la velocidad de muestreo deben cumplir una de las configuraciones de propiedades devueltas.

El autor de la llamada es responsable de liberar la memoria asignada para esta estructura. La siguiente función muestra cómo borrar una estructura **de \_ \_ capacidad de formato WMDM** .


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_formulario de \_ \_ valores válidos prop \_ enum de \_ WMDM**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_configuración de propiedades de WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**Descripción de la Prop de WMDM \_ \_**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





