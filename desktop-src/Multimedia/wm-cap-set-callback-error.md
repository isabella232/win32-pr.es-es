---
title: Mensaje de WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: El \_ \_ \_ \_ mensaje de error de devolución de llamada de Cap de WM establece una función de devolución de llamada de error en la aplicación cliente. AVICap llama a este procedimiento cuando se producen errores. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Mensaje de WM_CAP_SET_CALLBACK_ERROR de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491140"
---
# <a name="wm_cap_set_callback_error-message"></a>\_Mensaje de \_ \_ error de devolución de llamada de límite de WM \_

El mensaje de **\_ error de devolución de \_ \_ llamada \_ de Cap de WM** establece una función de devolución de llamada de error en la aplicación cliente. AVICap llama a este procedimiento cuando se producen errores. Puede enviar este mensaje explícitamente o mediante la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de error, de tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Especifique **null** para este parámetro para deshabilitar una función de devolución de llamada de error instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** si la captura de streaming o una sesión de captura de un solo fotograma está en curso.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer opcionalmente una función de devolución de llamada de error. Si se establece, AVICap llama al procedimiento de error en las situaciones siguientes:

-   El disco está lleno.
-   No se puede conectar una ventana de captura con un controlador de captura.
-   No se puede abrir un dispositivo de audio de onda.
-   El número de fotogramas descartados durante la captura supera el porcentaje especificado.
-   Los fotogramas no se pueden capturar debido a problemas de interrupción de sincronización verticales.

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

 

 





