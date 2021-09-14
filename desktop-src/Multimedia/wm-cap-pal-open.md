---
title: WM_CAP_PAL_OPEN mensaje (Vfw.h)
description: El mensaje WM CAP PAL OPEN carga una nueva paleta de un archivo de paleta \_ y la pasa a un controlador de \_ \_ captura.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161355"
---
# <a name="wm_cap_pal_open-message"></a>Mensaje \_ DE WM CAP PAL \_ \_ OPEN

El **mensaje WM CAP PAL \_ \_ \_ OPEN** carga una nueva paleta de un archivo de paleta y la pasa a un controlador de captura. Normalmente, los archivos de paleta usan la extensión de nombre de archivo . CAMARADA. Un controlador de captura usa una paleta cuando lo requiere el formato de imagen digitalizado especificado. Puede enviar este mensaje explícitamente o mediante la [**macro capPaletteOpen.**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen)


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre de archivo de la paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

Si se produce un error y se establece una función de devolución de llamada de error mediante el mensaje [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) se llama a la función de devolución de llamada de error.

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

 

 





