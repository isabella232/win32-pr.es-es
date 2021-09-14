---
title: WM_CAP_SET_CALLBACK_ERROR mensaje (Vfw.h)
description: El mensaje WM CAP SET CALLBACK ERROR establece una función de devolución \_ de llamada de error en la aplicación \_ \_ \_ cliente. AVICap llama a este procedimiento cuando se producen errores. Puede enviar este mensaje explícitamente o mediante la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161340"
---
# <a name="wm_cap_set_callback_error-message"></a>Mensaje \_ DE ERROR DE \_ \_ DEVOLUCIÓN DE LLAMADA \_ DE WM CAP SET

El **mensaje WM CAP SET \_ \_ \_ CALLBACK \_ ERROR** establece una función de devolución de llamada de error en la aplicación cliente. AVICap llama a este procedimiento cuando se producen errores. Puede enviar este mensaje explícitamente o mediante la [**macro capSetCallbackOnError.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror)


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntero a la función de devolución de llamada de error, de tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Especifique **NULL para** este parámetro para deshabilitar una función de devolución de llamada de error instalada previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **si** la captura de streaming o una sesión de captura de un solo fotograma están en curso.

## <a name="remarks"></a>Observaciones

Opcionalmente, las aplicaciones pueden establecer una función de devolución de llamada de error. Si se establece, AVICap llama al procedimiento de error en las situaciones siguientes:

-   El disco está lleno.
-   Una ventana de captura no se puede conectar con un controlador de captura.
-   No se puede abrir un dispositivo de audio de forma de onda.
-   El número de fotogramas descartados durante la captura supera el porcentaje especificado.
-   Los fotogramas no se pueden capturar debido a problemas de interrupción de la sincronización vertical.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





