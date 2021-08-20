---
description: El tipo de \_ enumeración WPD FOCUS \_ MODES describe el modo de enfoque que usa un dispositivo de captura de imágenes fijas.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: WPD_FOCUS_MODES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 87dca9643174b9497e0643d1c0fdcfcd8c57c18e638f7cf8441ea08b8e958a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026352"
---
# <a name="wpd_focus_modes-enumeration"></a>Enumeración \_ WPD FOCUS \_ MODES

El **tipo de \_ enumeración \_ WPD FOCUS MODES** describe el modo de enfoque que usa un dispositivo de captura de imágenes fijas.

## <a name="syntax"></a>Syntax


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

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD \_ FOCUS \_ UNDEFINED**
</dt> <dd>

No se ha especificado el modo de enfoque.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**MANUAL DE \_ FOCO DE \_ WPD**
</dt> <dd>

Especifica el foco manual.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD \_ FOCUS \_ AUTOMATIC**
</dt> <dd>

Especifica el foco automático, controlado por el dispositivo.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD \_ FOCUS \_ AUTOMATIC \_ MACRO**
</dt> <dd>

Especifica que el dispositivo debe cambiar automáticamente entre macro y foco normal, según sea necesario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad \_ WPD STILL \_ IMAGE FOCUS \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




