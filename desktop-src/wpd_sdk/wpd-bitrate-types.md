---
description: El tipo de \_ enumeración WPD BITRATE \_ TYPES describe un tipo de compresión de archivos de audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704055"
---
# <a name="wpd_bitrate_types-enumeration"></a>Enumeración \_ WPD BITRATE \_ TYPES

El **tipo de \_ enumeración \_ WPD BITRATE TYPES** describe el tipo de compresión de un archivo de audio.

## <a name="syntax"></a>Syntax


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

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**TIPO DE \_ VELOCIDAD DE BITS \_ WPD SIN \_ USAR**
</dt> <dd>

Este valor no se ha especificado.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD \_ BITRATE \_ TYPE \_ DISCRETE**
</dt> <dd>

Compresión de velocidad de bits constante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABLE DE TIPO \_ DE VELOCIDAD DE BITS \_ \_ WPD**
</dt> <dd>

Compresión de velocidad de bits variable.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD \_ BITRATE \_ TYPE \_ FREE**
</dt> <dd>

Velocidad de bits de formato libre. Se trata de una velocidad de bits constante inferior a la velocidad de bits máxima permitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




