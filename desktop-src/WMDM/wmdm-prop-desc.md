---
title: WMDM_PROP_DESC estructura
description: La estructura DESC PROP de WMDM \_ describe los valores \_ válidos de una propiedad en una configuración de propiedad determinada.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC estructura windows Media Administrador de dispositivos
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
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903945"
---
# <a name="wmdm_prop_desc-structure"></a>Estructura \_ DESC de WMDM PROP \_

La **estructura \_ \_ DESC PROP de WMDM** describe los valores válidos de una propiedad en una configuración de propiedad determinada.

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

Nombre de la propiedad. La aplicación debe liberar esta memoria cuando haya terminado de usarlo.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Valor [**de enumeración \_ WMDM ENUM \_ PROP VALID VALUES \_ \_ \_ FORM**](wmdm-enum-prop-valid-values-form.md) que describe el tipo de valores, como un intervalo o una lista. El valor de esta enumeración determina qué variable miembro se utiliza.

</dd> <dt>

**ValidValues**
</dt> <dd>

Contiene los valores válidos de la propiedad en una configuración de propiedad determinada. Este miembro contiene uno de tres elementos: el valor de enumeración WMDM ENUM PROP VALID VALUES ANY; el miembro ValidValuesRange o el miembro \_ \_ \_ \_ \_ **EnumeratedValidValues**.  **ValidValuesForm** indica el valor o miembro .

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Estructura [**RANGE DE VALORES DE PROP \_ \_ \_ de WMDM**](wmdm-prop-values-range.md) que contiene un intervalo de valores válidos. Esto solo está presente cuando **ValidValuesForm** se establece en WMDM \_ ENUM \_ PROP VALID \_ VALUES \_ \_ RANGE. Vea la sección Comentarios.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Estructura [**\_ \_ \_ ENUM DE VALORES DE PROP DE WMDM**](wmdm-prop-values-enum.md) que contiene un conjunto enumerado de valores válidos. Esto solo está presente cuando **ValidValuesForm** se establece en WMDM \_ ENUM \_ PROP VALID \_ VALUES \_ \_ ENUM. Vea la sección Comentarios.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ \_ DESC PROP de WMDM** contiene una descripción de propiedad que consta de un nombre de propiedad y sus valores válidos en una configuración determinada.

El autor de la llamada debe liberar la memoria utilizada por **ValidValuesRange** **o EnumeratedValues.** Para obtener un ejemplo de cómo hacerlo, vea [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**ENUMERACIÓN DE \_ VALORES \_ DE PROP \_ DE WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALO DE VALORES \_ DE \_ PROPIEDAD DE \_ WMDM**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





