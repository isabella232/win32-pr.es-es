---
description: El \_ tipo de \_ enumeración de valores de tipo de almacenamiento WPD \_ describe los distintos tipos de almacenamiento de dispositivos portátiles de Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumeración WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
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
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649867"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_ \_ Enumeración de valores de tipo de almacenamiento WPD \_

El tipo de enumeración de **\_ valores de \_ tipo \_ de almacenamiento WPD** describe los distintos tipos de almacenamiento de dispositivos portátiles de Windows.

## <a name="syntax"></a>Sintaxis


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

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**tipo de almacenamiento de WPD sin \_ \_ \_ definir**
</dt> <dd>

El almacenamiento es de un tipo no definido.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**tipo de almacenamiento WPD de \_ \_ \_ \_ ROM fijo**
</dt> <dd>

El almacenamiento no es extraíble y de solo lectura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ ROM extraíble del tipo de almacenamiento de \_ WPD \_**
</dt> <dd>

El almacenamiento es extraíble y es de solo lectura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ \_ memoria RAM fija de tipo de almacenamiento WPD \_**
</dt> <dd>

El almacenamiento no es extraíble y es compatible con lectura y escritura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ memoria RAM extraíble del tipo de almacenamiento WPD \_**
</dt> <dd>

El almacenamiento es extraíble y es compatible con lectura y escritura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




