---
title: Mensaje de WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: El \_ mensaje AUDIOFORMAT de Cap de WM \_ \_ establece el formato de audio que se va a usar al realizar la captura de flujo o paso. Puede enviar este mensaje explícitamente o mediante la macro capSetAudioFormat.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- Mensaje de WM_CAP_SET_AUDIOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150443"
---
# <a name="wm_cap_set_audioformat-message"></a>\_ \_ Mensaje AUDIOFORMAT de conjunto de Cap de WM \_

El **mensaje \_ \_ \_ AUDIOFORMAT de Cap de WM** establece el formato de audio que se va a usar al realizar la captura de flujo o paso. Puede enviar este mensaje explícitamente o mediante la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamaño, en bytes, de la estructura a la que hace referencia **s**.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

Puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) que define el formato de audio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

