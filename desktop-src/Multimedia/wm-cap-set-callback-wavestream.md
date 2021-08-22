---
title: WM_CAP_SET_CALLBACK_WAVESTREAM mensaje (Vfw.h)
description: El mensaje WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM establece una función de devolución de llamada en la aplicación.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM mensaje Windows Multimedia
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
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622524"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>Mensaje \_ \_ WAVESTREAM DE \_ DEVOLUCIÓN DE LLAMADA DE \_ WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ WAVESTREAM** establece una función de devolución de llamada en la aplicación. AVICap llama a este procedimiento durante la captura de streaming cuando hay disponible un nuevo búfer de audio. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnWaveStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream)


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de flujo de onda, de tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada de flujo de onda instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza **correctamente o FALSE si** la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

La ventana de captura llama al procedimiento antes de escribir el búfer de audio en el disco. Esto permite a las aplicaciones modificar el búfer de audio si lo desea.

Si se usa una función de devolución de llamada de flujo de onda, debe instalarse antes de iniciar la sesión de captura y debe permanecer habilitada mientras dure la sesión. Se puede deshabilitar una vez que finaliza la captura de streaming.

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

 

 





