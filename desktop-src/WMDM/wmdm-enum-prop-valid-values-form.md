---
title: WMDM_ENUM_PROP_VALID_VALUES_FORM enumeración
description: El tipo de enumeración \_ WMDM ENUM PROP VALID VALUES FORM describe las \_ \_ \_ \_ posibles formas de valores válidos para una propiedad.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM enumeración windows Media Administrador de dispositivos
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
ms.openlocfilehash: b59ad120fee9faf9b6cc8eb62afacd61dcb73586f6a6314988ee7ff34be05732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055553"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>Enumeración FORM DE VALORES VÁLIDOS DE PROP DE WMDM \_ ENUM \_ \_ \_ \_

El **tipo de enumeración \_ WMDM ENUM \_ PROP VALID VALUES \_ \_ \_ FORM** describe las posibles formas de valores válidos para una propiedad.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ ENUM \_ PROP \_ VALID \_ VALUES \_ ANY**
</dt> <dd>

Todos los valores son válidos.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**INTERVALO DE VALORES \_ VÁLIDOS DE \_ PROP DE \_ \_ ENUMERACIÓN WMDM \_**
</dt> <dd>

Los valores válidos se expresan como un intervalo. Para obtener información detallada, vea la estructura [**WMDM \_ PROP VALUES \_ \_ RANGE.**](wmdm-prop-values-range.md)

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**ENUMERACIÓN WMDM \_ \_ PROP VALID VALUES \_ \_ \_ ENUM**
</dt> <dd>

Los valores válidos son un conjunto enumerado. Para obtener información detallada, vea la estructura [**\_ \_ \_ ENUM WMDM PROP VALUES.**](wmdm-prop-values-enum.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración se usa en la [**estructura \_ \_ DESC PROP de WMDM**](wmdm-prop-desc.md) para especificar la forma de valores válidos para una propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**FUNCIONALIDAD DE \_ FORMATO \_ WMDM**](wmdm-format-capability.md)
</dt> <dt>

[**CONFIGURACIÓN DE PROP DE WMDM \_ \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERACIÓN DE \_ VALORES PROP \_ \_ DE WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALO DE VALORES \_ DE PROPIEDAD \_ DE WMDM \_**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





