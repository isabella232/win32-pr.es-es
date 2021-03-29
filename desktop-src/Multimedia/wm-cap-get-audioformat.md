---
title: Mensaje de WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: El \_ mensaje Cap \_ \_ AUDIOFORMAT de WM obtiene el formato de audio o el tamaño del formato de audio. Puede enviar este mensaje explícitamente o mediante las macros capGetAudioFormat y capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- Mensaje de WM_CAP_GET_AUDIOFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421907"
---
# <a name="wm_cap_get_audioformat-message"></a>\_Mensaje Cap \_ Get \_ AUDIOFORMAT de WM

El **mensaje \_ Cap \_ \_ AUDIOFORMAT de WM** obtiene el formato de audio o el tamaño del formato de audio. Puede enviar este mensaje explícitamente o mediante las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .


```C++
WM_CAP_GET_AUDIOFORMAT 
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

Puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o **null**. Si el valor es **null**, se devuelve el tamaño, en bytes, necesario para contener la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes, del formato de audio.

## <a name="remarks"></a>Observaciones

Dado que los formatos de audio comprimidos varían en cuanto a los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar la memoria y, por último, solicitar los datos del formato de audio.

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

 

