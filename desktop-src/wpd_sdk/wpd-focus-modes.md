---
description: El \_ tipo de enumeración de modos de enfoque de WPD \_ describe el modo de enfoque utilizado por un dispositivo de captura de imagen fija.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumeración WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671011"
---
# <a name="wpd_focus_modes-enumeration"></a>\_Enumeración de modos de enfoque de WPD \_

El tipo de enumeración de **\_ \_ modos de enfoque de WPD** describe el modo de enfoque utilizado por un dispositivo de captura de imagen fija.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**enfoque de WPD \_ \_ sin definir**
</dt> <dd>

No se ha especificado el modo de enfoque.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_manual del foco de WPD \_**
</dt> <dd>

Especifica el foco manual.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_enfoque \_ automático de WPD**
</dt> <dd>

Especifica el foco automático, controlado por el dispositivo.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automática de foco de WPD \_**
</dt> <dd>

Especifica que el dispositivo debe cambiar automáticamente entre la macro y el foco normal, según sea necesario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la propiedad del modo de enfoque de imagen de la [ \_ \_ imagen \_ \_ de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




