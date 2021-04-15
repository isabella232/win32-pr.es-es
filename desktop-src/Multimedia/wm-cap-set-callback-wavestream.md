---
title: Mensaje de WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: El \_ \_ \_ \_ mensaje WAVESTREAM de devolución de llamada del conjunto de Cap de WM establece una función de devolución de llamada en la aplicación.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_WAVESTREAM de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492947"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>\_Mensaje de \_ \_ error de devolución de llamada de Cap de WM \_

El **mensaje \_ WAVESTREAM de \_ devolución de \_ llamada \_ del conjunto de Cap de WM** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento durante la captura de streaming cuando un nuevo búfer de audio está disponible. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de flujo de onda, de tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de flujo de onda instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

La ventana captura llama al procedimiento antes de escribir el búfer de audio en el disco. Esto permite que las aplicaciones modifiquen el búfer de audio si se desea.

Si se utiliza una función de devolución de llamada de flujo de onda, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión. Se puede deshabilitar después de que finalice la captura de streaming.

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

 

 





