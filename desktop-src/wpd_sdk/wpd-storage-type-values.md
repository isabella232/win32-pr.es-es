---
description: El tipo de enumeración WPD STORAGE TYPE VALUES describe los distintos tipos Windows almacenamiento de \_ \_ \_ dispositivos portátiles.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: WPD_STORAGE_TYPE_VALUES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842082"
---
# <a name="wpd_storage_type_values-enumeration"></a>Enumeración \_ WPD STORAGE \_ TYPE \_ VALUES

El **tipo de \_ enumeración WPD STORAGE \_ TYPE \_ VALUES** describe los distintos tipos Windows almacenamiento de dispositivos portátiles.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**TIPO DE \_ ALMACENAMIENTO WPD \_ SIN \_ DEFINIR**
</dt> <dd>

El almacenamiento es de un tipo no definido.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD \_ STORAGE \_ TYPE \_ FIXED \_ ROM**
</dt> <dd>

El almacenamiento no es extraíble y de solo lectura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD \_ STORAGE \_ TYPE \_ REMOVABLE \_ ROM**
</dt> <dd>

El almacenamiento es extraíble y es de solo lectura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**RAM FIJA \_ DE TIPO DE ALMACENAMIENTO \_ \_ \_ WPD**
</dt> <dd>

El almacenamiento no es extraíble y es compatible con lectura y escritura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**RAM EXTRAÍBLE DE TIPO DE ALMACENAMIENTO \_ \_ \_ \_ WPD**
</dt> <dd>

El almacenamiento es extraíble y es compatible con lectura y escritura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




