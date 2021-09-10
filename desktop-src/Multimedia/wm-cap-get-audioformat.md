---
title: WM_CAP_GET_AUDIOFORMAT mensaje (Vfw.h)
description: El mensaje GET AUDIOFORMAT de WM \_ CAP obtiene el formato de audio o el tamaño del formato de \_ \_ audio. Puede enviar este mensaje explícitamente o mediante las macros capGetAudioFormat y capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371444"
---
# <a name="wm_cap_get_audioformat-message"></a>Mensaje \_ GET \_ AUDIOFORMAT de WM CAP \_

El **mensaje \_ GET \_ \_ AUDIOFORMAT** de WM CAP obtiene el formato de audio o el tamaño del formato de audio. Puede enviar este mensaje explícitamente o mediante las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize)


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

Puntero a una [**estructura DESATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) O **NULL.** Si el valor es **NULL,** se devuelve el tamaño, en bytes, necesario para contener la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes, del formato de audio.

## <a name="remarks"></a>Observaciones

Dado que los formatos de audio comprimido varían en los requisitos de tamaño, las aplicaciones deben recuperar primero el tamaño, asignar memoria y, por último, solicitar los datos de formato de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

