---
title: Enumeración WMDM_ENUM_PROP_VALID_VALUES_FORM
description: El \_ \_ \_ \_ \_ tipo de enumeración de formulario de valores válidos prop enum de WMDM describe posibles formas de valores válidos para una propiedad.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Enumeración WMDM_ENUM_PROP_VALID_VALUES_FORM Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698618"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>\_ \_ \_ \_ Enumeración del formulario de valores válidos prop enum de WMDM \_

El tipo de enumeración de **\_ \_ \_ \_ \_ formulario de valores válidos prop enum de WMDM** describe posibles formas de valores válidos para una propiedad.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**\_ \_ \_ valores válidos de \_ la enumeración WMDM \_**
</dt> <dd>

Todos los valores son válidos.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_intervalo de \_ \_ valores válidos prop \_ enum de \_ WMDM**
</dt> <dd>

Los valores válidos se expresan como un intervalo. Para obtener información detallada, consulte la estructura de [**intervalo de valores de propiedades de WMDM \_ \_ \_**](wmdm-prop-values-range.md) .

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**enumeración de \_ \_ \_ valores válidos prop \_ \_ enum de WMDM**
</dt> <dd>

Los valores válidos son un conjunto enumerado. Para obtener información detallada, consulte la estructura de [**\_ \_ \_ enumeración de valores de propiedades de WMDM**](wmdm-prop-values-enum.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la estructura de [**\_ \_ Descripción**](wmdm-prop-desc.md) de la propiedad WMDM para especificar el formato de los valores válidos de una propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_funcionalidad de formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**\_configuración de propiedades de WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**Descripción de la Prop de WMDM \_ \_**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





