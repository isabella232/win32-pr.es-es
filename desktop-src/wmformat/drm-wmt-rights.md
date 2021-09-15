---
title: WMT_RIGHTS enumeración (Wmdrmsdk.h)
description: Define los derechos que se pueden especificar en una licencia DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS enumeración windows Media Format
- enumeración windows Media Format
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466713"
---
# <a name="wmt_rights-enumeration"></a>Enumeración DE DERECHOS DE WMT \_

El **tipo de \_ enumeración WMT RIGHTS** define los derechos que se pueden especificar en una licencia DRM.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**REPRODUCCIÓN DERECHA DE WMT \_ \_**
</dt> <dd>

Especifica el derecho a reproducir contenido sin restricciones.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**COPIA CON \_ EL BOTÓN \_ DERECHO WMT EN UN \_ DISPOSITIVO QUE NO ES \_ \_ \_ SDMI**
</dt> <dd>

Especifica el derecho a copiar contenido en un dispositivo no compatible con secure digital Música Initiative (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**COPIA DERECHA DE WMT \_ \_ EN \_ \_ CD**
</dt> <dd>

Especifica el derecho a copiar contenido en un CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**COPIA DERECHA DE WMT \_ \_ EN EL DISPOSITIVO \_ \_ \_ SDMI**
</dt> <dd>

Especifica el derecho a copiar contenido en un dispositivo compatible con sdmi.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**DERECHO DE WMT \_ \_ UNA \_ VEZ**
</dt> <dd>

Especifica el derecho a reproducir contenido solo una vez.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**GUARDAR \_ SECUENCIA PROTEGIDA CON \_ EL BOTÓN DERECHO \_ DE \_ WMT**
</dt> <dd>

Especifica el derecho para guardar contenido de un servidor.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**COPIA DERECHA DE WMT \_ \_**
</dt> <dd>

Especifica el derecho para copiar contenido. Windows Drm multimedia 10 regula los dispositivos en los que se puede copiar el contenido mediante los niveles de protección de salida (OLO).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ RIGHT \_ COLLABORATIVE \_ PLAY**
</dt> <dd>

Especifica el derecho a reproducir contenido como parte de un escenario en línea en el que varios participantes pueden aportar canciones de su colección a una lista de reproducción compartida.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**DESENCADENADOR DE \_ \_ SDMI DERECHO DE WMT \_**
</dt> <dd>

Reservado para uso futuro. No debe usarse.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ RIGHT \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

Reservado para uso futuro. No debe usarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos valores son marcas de bits, por lo que se puede establecer una o varias mediante su combinación con el operador **OR** bit a bit.

Cuando se usa Windows Media DRM 10, **WMT \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE**, **WMT RIGHT COPY TO \_ \_ \_ \_ SDMI \_ DEVICE** y **WMT RIGHT COPY TO \_ \_ \_ \_ CD** se reemplazan por **WMT RIGHT \_ \_ COPY**. Las limitaciones de los dispositivos en los que se puede copiar el contenido se especifican mediante los niveles de protección de salida (OCL).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





