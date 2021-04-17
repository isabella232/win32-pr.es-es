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
# <a name="wmdm_prop_values_range-structure"></a>\_Estructura de \_ intervalo de valores de prop de WMDM \_

La estructura de intervalo de valores de prop de WMDM describe un intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**rangeMin**
</dt> <dd>

Valor mínimo del intervalo.

</dd> <dt>

**rangeMax**
</dt> <dd>

Valor máximo del intervalo.

</dd> <dt>

**rangeStep**
</dt> <dd>

Tamaño del paso en el que los valores válidos aumentan desde el valor mínimo hasta el valor máximo. Esto permite especificar valores permitidos discretos en un intervalo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa en la estructura de [**\_ \_ Descripción**](wmdm-prop-desc.md) de la props de WMDM para describir un intervalo de valores válidos. Un intervalo de valores válidos es aplicable cuando \_ \_ se selecciona la enumeración de valores válidos prop enum de WMDM \_ \_ \_ en la enumeración de WMDM enumeración de valores [**\_ \_ \_ válidos \_ \_ prop**](wmdm-enum-prop-valid-values-form.md) .

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

[**\_configuración de propiedades de WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**Descripción de la Prop de WMDM \_ \_**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





