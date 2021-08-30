---
title: WMDM_FORMAT_CAPABILITY estructura
description: La estructura \_ WMDM FORMAT \_ CAPABILITY describe las funciones de un dispositivo para un formato determinado.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY estructura windows Media Administrador de dispositivos
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
ms.openlocfilehash: c42c654bc07e6e47e5ead5b374f6cd16b20c2fc3e36433eb68006b1e270c1ca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004805"
---
# <a name="wmdm_format_capability-structure"></a>Estructura DE \_ CAPACIDAD DE FORMATO \_ WMDM

La **estructura \_ WMDM FORMAT \_ CAPABILITY** describe las funciones de un dispositivo para un formato determinado. Esta estructura contiene un conjunto de configuraciones de propiedades en una matriz de estructuras **DE CONFIGURACIÓN DE PROP \_ \_ de WMDM.** Cada configuración de propiedad representa un conjunto de valores de propiedad compatibles en todas las propiedades admitidas para un formato determinado. La aplicación puede obtener esta estructura llamando al método **IWMDMDevice3::GetFormatCapability** y pasando el código de formato. Para obtener una lista de códigos de formato, vea [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).

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

Número de configuraciones de propiedades en la **matriz pConfigs.**

</dd> <dt>

**pConfigs**
</dt> <dd>

Puntero a una matriz de [**estructuras DE CONFIGURACIÓN DE PROP \_ \_ de WMDM.**](wmdm-prop-config.md) El tamaño de la matriz es igual al valor de **nPropConfig**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ WMDM FORMAT \_ CAPABILITY** proporciona un mecanismo flexible para expresar las funcionalidades del dispositivo para un formato determinado.

Si el dispositivo va a representar el contenido (por ejemplo, un archivo de audio que va a reproducir el dispositivo), las propiedades del contenido deben coincidir con una de las configuraciones de propiedades devueltas por [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) en la estructura **WMDM \_ FORMAT \_ CAPABILITY.** Por ejemplo, para un archivo de audio, la velocidad de bits y la frecuencia de muestreo deben satisfacer una de las configuraciones de propiedad devueltas.

El autor de la llamada es responsable de liberar la memoria asignada para esta estructura. La siguiente función muestra cómo borrar una estructura **WMDM \_ FORMAT \_ CAPABILITY.**


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
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**FORMULARIO DE VALORES \_ VÁLIDOS DE \_ PROP DE \_ \_ ENUMERACIÓN WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**CONFIGURACIÓN DE PROP DE WMDM \_ \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERACIÓN DE \_ VALORES PROP \_ \_ DE WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALO DE VALORES \_ DE PROPIEDAD \_ DE WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





