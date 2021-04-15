---
title: Enumeración WMT_RIGHTS (wmdrmsdk. h)
description: Define los derechos que se pueden especificar en una licencia de DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS enumeración formato de Windows Media
- enumeración Windows Media Format
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708141"
---
# <a name="wmt_rights-enumeration"></a>\_Enumeración de derechos WMT

El tipo de enumeración de **\_ derechos WMT** define los derechos que se pueden especificar en una licencia de DRM.

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

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**\_reproducción correcta de WMT \_**
</dt> <dd>

Especifica el derecho para reproducir contenido sin restricciones.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_copia derecha \_ \_ de WMT en un \_ dispositivo que no es de \_ SDMI \_**
</dt> <dd>

Especifica el derecho para copiar contenido en un dispositivo no compatible con la iniciativa de música digital segura (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**\_copia correcta del WMT \_ \_ en el \_ CD**
</dt> <dd>

Especifica el derecho para copiar contenido en un CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_copia correcta \_ \_ de WMT en el \_ dispositivo de SDMI \_**
</dt> <dd>

Especifica el derecho para copiar contenido en un dispositivo compatible con SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ justo \_ una \_ vez**
</dt> <dd>

Especifica el derecho para reproducir contenido solo una vez.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**la \_ secuencia de guardado del derecho WMT está \_ \_ \_ protegida**
</dt> <dd>

Especifica el derecho para guardar el contenido de un servidor.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**\_copia correcta de WMT \_**
</dt> <dd>

Especifica el derecho para copiar contenido. Windows Media DRM 10 regula los dispositivos en los que se puede copiar el contenido mediante el uso de los niveles de protección de salida (OPLs).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**\_ \_ reproducción colaborativa correcta de WMT \_**
</dt> <dd>

Especifica el derecho para reproducir contenido como parte de un escenario en línea en el que varios participantes pueden aportar canciones de su colección a una lista de reproducción compartida.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_ \_ desencadenador de SDMI de la derecha WMT \_**
</dt> <dd>

Reservado para uso futuro. No debe usarse.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

Reservado para uso futuro. No debe usarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos valores son marcas de bits, por lo que se pueden establecer uno o varios combinando con **el operador OR** bit a bit.

Al usar Windows Media DRM 10, **la \_ \_ copia correcta \_ de WMT en un \_ \_ \_ dispositivo que no es de SDMI**, la **\_ \_ copia correcta de WMT en el \_ \_ \_ dispositivo de SDMI** y la **\_ \_ copia correcta de WMT en el \_ \_ CD** se sustituyen por la **\_ \_ copia correcta de WMT**. Las limitaciones de los dispositivos en los que se puede copiar el contenido se especifican mediante los niveles de protección de la salida (OPLs).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





