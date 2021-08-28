---
description: Define códigos de error de clave multimedia para el motor de medios.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 5a3573f721f31ffbe3858c7d6fb3c713468bc347f04a1b5d85c5839a1e18511b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113935"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>MF \_ MEDIA \_ ENGINE \_ KEYERR (enumeración)

Define códigos de error de clave multimedia para el motor de medios.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ UNKNOWN**
</dt> <dd>

Error desconocido.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ CLIENT**
</dt> <dd>

Error con el cliente.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**SERVICIO \_ MF MEDIAENGINE \_ \_ KEYERR**
</dt> <dd>

Se produjo un error con el servicio.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**SALIDA \_ DE MF MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Error con la salida.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Error relacionado con un cambio de hardware.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**DOMINIO \_ \_ KEYERR DE MF MEDIAENGINE \_**
</dt> <dd>

Error con el dominio.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**MF \_ MEDIA \_ ENGINE \_ KEYERR se** usa con el parámetro de código de  [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) y el valor de código devuelto de [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md). 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation enumeraciones](media-foundation-enumerations.md)
</dt> </dl>

 

 




