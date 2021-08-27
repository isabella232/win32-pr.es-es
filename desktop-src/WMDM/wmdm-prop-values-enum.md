---
title: WMDM_PROP_VALUES_ENUM estructura
description: La estructura ENUM DE VALORES DE PROP DE WMDM contiene un conjunto enumerado de valores válidos para \_ una propiedad determinada en una configuración de propiedad \_ \_ determinada.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM estructura windows Media Administrador de dispositivos
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
ms.openlocfilehash: 35766ed71b864c5eb7f0bbbebf5eda384a25e174501aa2a56e790840a4c636c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004795"
---
# <a name="wmdm_prop_values_enum-structure"></a>Estructura \_ ENUM DE VALORES \_ DE PROP \_ DE WMDM

La **estructura \_ \_ \_ ENUM DE VALORES DE** PROP DE WMDM contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.

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

Puntero a una matriz de valores. El tamaño de la matriz es igual al valor de **cEnumValues.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en la estructura **\_ \_ DESC PROP de WMDM** para describir un conjunto enumerado de valores válidos. Un conjunto enumerado de valores válidos es aplicable cuando se selecciona \_ \_ ENUM ENUM PROP VALID VALUES ENUM de \_ \_ \_ **WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM** enumeración.

El autor de la llamada es necesario para liberar la memoria utilizada por **pValues.** Para obtener un ejemplo de cómo hacerlo, vea [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**INTERVALO DE VALORES \_ DE \_ PROPIEDAD DE \_ WMDM**](wmdm-prop-values-range.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





