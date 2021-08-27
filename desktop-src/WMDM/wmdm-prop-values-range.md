---
title: WMDM_PROP_VALUES_RANGE estructura
description: La estructura RANGE DE VALORES DE PROPIEDAD DE WMDM describe un intervalo de valores \_ \_ \_ válidos para una propiedad determinada en una configuración de propiedad determinada.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE estructura windows Media Administrador de dispositivos
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
ms.openlocfilehash: a668b5acd8427df5b4bc163788c225f4eaee9a16b70af25312ae8ec94cb2bb63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004785"
---
# <a name="wmdm_prop_values_range-structure"></a>Estructura DE \_ INTERVALOS DE VALORES \_ DE PROP \_ DE WMDM

La **estructura RANGE DE VALORES DE PROP \_ \_ \_ de WMDM** describe un intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada.

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

Valor mínimo en el intervalo.

</dd> <dt>

**Rangemax**
</dt> <dd>

Valor máximo del intervalo.

</dd> <dt>

**rangeStep**
</dt> <dd>

Tamaño del paso en el que los valores válidos se incrementan del valor mínimo al valor máximo. Esto permite especificar valores discretos permitidos en un intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en la estructura [**\_ \_ DESC PROP de WMDM**](wmdm-prop-desc.md) para describir un intervalo de valores válidos. Se aplica un intervalo de valores válidos cuando se selecciona ENUM VALORES VÁLIDOS DE PROP DE WMDM ENUM de la enumeración \_ \_ \_ \_ \_ [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM.**](wmdm-enum-prop-valid-values-form.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**FORMATO DE VALORES \_ VÁLIDOS \_ DE PROP DE \_ \_ ENUMERACIÓN WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**FUNCIONALIDAD DE FORMATO WMDM \_ \_**](wmdm-format-capability.md)
</dt> <dt>

[**CONFIGURACIÓN DE PROP de WMDM \_ \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERACIÓN DE \_ VALORES \_ DE PROP \_ DE WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





