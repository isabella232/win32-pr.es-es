---
title: ICM_DRAW mensaje (Vfw.h)
description: El ICM DRAW notifica a un controlador de representación que descomprima un fotograma de datos y \_ lo dibuja en la pantalla.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246290"
---
# <a name="icm_draw-message"></a>\_ICM Draw message (Mensaje DRAW)

El **ICM \_ draw notifica** a un controlador de representación que descomprima un marco de datos y lo dibuja en la pantalla.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Puntero a una [**estructura ICDRAW.**](/windows/desktop/api/Vfw/ns-vfw-icdraw)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDRAW.**](/windows/desktop/api/Vfw/ns-vfw-icdraw)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si la marca ICDRAW UPDATE se establece en el miembro \_ **dwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), el área de la pantalla usada para dibujar no es válida y debe actualizarse. La extensión de la actualización depende del contenido del **miembro lpData.**

Si **lpData** es **NULL,** el controlador debe actualizar todo el rectángulo de destino con la imagen actual. Si el controlador mantiene una copia de la imagen en un búfer fuera de la pantalla, puede producir un error en este mensaje. Si **lpData** no es **NULL,** el controlador debe dibujar los datos y asegurarse de que se actualiza todo el destino.

Si la marca ICDRAW DENSEUP se establece en dwFlags , la aplicación que realiza la llamada quiere que el controlador continúe lo más rápido posible, posiblemente ni siquiera \_ actualizando la pantalla.

Si la marca ICDRAW PREROLL está establecida en dwFlags , este fotograma de vídeo es información preliminar y no debe \_ mostrarse si es posible.  Por ejemplo, si la reproducción se inicia desde el fotograma 10 y el fotograma 0 es el fotograma clave anterior más cercano, los fotogramas del 0 al 9 tendrán establecido ICDRAW \_ PREROLL.

Si desea que el controlador descomprima los datos en un búfer, envíe el [**mensaje ICM \_ DECOMPRESS.**](icm-decompress.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





