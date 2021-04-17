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
# <a name="wmdm_prop_config-structure"></a>Estructura de configuración de \_ propiedades de WMDM \_

La estructura de **\_ \_ configuración de propiedades de WMDM** describe un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con el dispositivo para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras de propiedades [**\_ \_ DESC de WMDM**](wmdm-prop-desc.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nPreference**
</dt> <dd>

Nivel de preferencia del dispositivo para esta configuración. El valor más bajo indica la configuración preferida.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Número de descripciones de propiedad contenidas en esta configuración. Hay una única descripción de propiedad para cada propiedad admitida para el formato especificado.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Puntero a una matriz de estructuras de tipo [**\_ \_ DESC de WMDM**](wmdm-prop-desc.md) que contienen descripciones de propiedades. El tamaño de la matriz es igual al valor de **nPropDesc**. La aplicación debe liberar esta memoria cuando termine.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de la [**\_ \_ capacidad del formato WMDM**](wmdm-format-capability.md) devuelta por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) para un formato determinado consta de varias configuraciones de propiedades. **WMDM \_ Las \_** estructuras de configuración de prop describen esas configuraciones.

Una configuración de propiedades describe los valores de todas las propiedades compatibles con un formato determinado. Los valores de propiedades diferentes en una sola configuración son compatibles entre sí. Por ejemplo, para un archivo de audio, una configuración incluirá valores válidos de la velocidad de muestra y valores válidos de la velocidad de bits, de modo que todas las combinaciones de estas velocidades de ejemplo y de bits se puedan reproducir en el dispositivo.

El llamador debe liberar la memoria usada por **pPropDesc**. Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).

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

[**\_funcionalidad de formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**Descripción de la Prop de WMDM \_ \_**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





