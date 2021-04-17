---
title: Estructura de WMDM_PROP_VALUES_ENUM
description: La \_ \_ \_ estructura de enumeración valores de prop de WMDM contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Estructura WMDM_PROP_VALUES_ENUM Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698738"
---
# <a name="wmdm_prop_values_enum-structure"></a>\_Estructura de \_ enumeración de valores de propiedades de WMDM \_

La estructura de **\_ \_ \_ enumeración valores de prop de WMDM** contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cEnumValues**
</dt> <dd>

Recuento de valores enumerados.

</dd> <dt>

**pValues**
</dt> <dd>

Puntero a una matriz de valores. El tamaño de la matriz es igual al valor de **cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa en la estructura de **\_ \_ Descripción** de la propiedades de WMDM para describir un conjunto enumerado de valores válidos. Se puede aplicar un conjunto enumerado de valores válidos si se selecciona la enumeración de la enumeración de valores válidos \_ \_ prop enum de WMDM \_ \_ \_ en la enumeración del **\_ \_ \_ \_ \_ formulario de valores válidos** de la enumeración WMDM.

El llamador debe liberar la memoria usada por **pValues**. Para obtener un ejemplo de cómo hacerlo, consulte [**funcionalidad de \_ formato \_ WMDM**](wmdm-format-capability.md).

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

[**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





