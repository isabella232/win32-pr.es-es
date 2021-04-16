---
description: El \_ tipo de enumeración de tipos de velocidad de bits de WPD \_ describe un tipo de compresión de archivos de audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumeración WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718939"
---
# <a name="wpd_bitrate_types-enumeration"></a>\_Enumeración de tipos de velocidad de bits de WPD \_

El tipo de enumeración de **\_ \_ tipos de velocidad de bits de WPD** describe el tipo de compresión de un archivo de audio.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**tipo de velocidad de bits de WPD \_ \_ \_ sin usar**
</dt> <dd>

No se ha especificado este valor.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_ \_ tipo discreto de velocidad de bits de WPD \_**
</dt> <dd>

Compresión de velocidad de bits constante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABLE de tipo de velocidad de bits de WPD \_ \_ \_**
</dt> <dd>

Compresión de velocidad de bits variable.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**tipo de velocidad de bits de WPD \_ \_ \_ gratis**
</dt> <dd>

Velocidad de bits de formato libre. Se trata de una velocidad de bits constante inferior a la velocidad de bits máxima permitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




