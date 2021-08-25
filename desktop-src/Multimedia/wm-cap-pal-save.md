---
title: WM_CAP_PAL_SAVE mensaje (Vfw.h)
description: El mensaje \_ SAVE de WM CAP PAL guarda la paleta actual en un archivo de \_ \_ paleta. Normalmente, los archivos de paleta usan la extensión de nombre de archivo . Camarada. Puede enviar este mensaje explícitamente o mediante la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff8703eafcc3c612fbde5bac7d15433758aa3d6ee44ab47697ffb25f9324dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891885"
---
# <a name="wm_cap_pal_save-message"></a>Mensaje \_ SAVE de WM CAP \_ PAL \_

El mensaje SAVE de **\_ WM CAP \_ PAL \_** guarda la paleta actual en un archivo de paleta. Normalmente, los archivos de paleta usan la extensión de nombre de archivo . Camarada. Puede enviar este mensaje explícitamente o mediante la [**macro capPaletteSave.**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave)


```C++
WM_CAP_PAL_SAVE 
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





