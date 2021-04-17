---
title: Estructura de WMDM_PROP_DESC
description: La \_ estructura de \_ Descripción de la propiedad WMDM describe los valores válidos de una propiedad en una configuración de propiedades determinada.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Estructura WMDM_PROP_DESC Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700176"
---
# <a name="wmdm_prop_desc-structure"></a>Estructura de descripción de la \_ propiedades WMDM \_

La estructura de **\_ \_ Descripción** de la propiedad WMDM describe los valores válidos de una propiedad en una configuración de propiedades determinada.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pwszPropName**
</dt> <dd>

Nombre de la propiedad. La aplicación debe liberar esta memoria cuando termine de usarla.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Un valor de enumeración de [**\_ \_ \_ \_ \_ formulario de valores válidos prop enum de WMDM**](wmdm-enum-prop-valid-values-form.md) que describe el tipo de valores, como un intervalo o una lista. El valor de esta enumeración determina qué variable miembro se utiliza.

</dd> <dt>

**ValidValues**
</dt> <dd>

Contiene los valores válidos de la propiedad en una configuración de propiedad determinada. Este miembro contiene uno de tres elementos: el valor de enumeración WMDM \_ Enumerate \_ \_ valores válidos \_ \_ Any; el miembro **ValidValuesRange**; o el miembro **EnumeratedValidValues**. El valor o el miembro está indicado por **ValidValuesForm**.

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Una estructura de intervalo de valores de propiedades de WMDM que contiene un intervalo de valores válidos. [**\_ \_ \_**](wmdm-prop-values-range.md) Solo está presente cuando **ValidValuesForm** se establece en la enumeración de WMDM de \_ \_ \_ valores válidos \_ \_ . Vea la sección Comentarios.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Estructura [**de \_ \_ \_ enumeración de valores de propiedades de WMDM**](wmdm-prop-values-enum.md) que contiene un conjunto enumerado de valores válidos. Esto solo está presente cuando **ValidValuesForm** se establece en la \_ enumeración de WMDM de \_ \_ valores válidos de enum \_ \_ . Vea la sección Comentarios.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de descripción de la propiedad **WMDM \_ \_** contiene una descripción de propiedad formada por un nombre de propiedad y sus valores válidos en una configuración determinada.

El llamador debe liberar la memoria usada por **ValidValuesRange** o **EnumeratedValues**. Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).

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

[**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





