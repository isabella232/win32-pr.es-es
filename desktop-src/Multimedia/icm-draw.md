---
title: Mensaje de ICM_DRAW (VFW. h)
description: El \_ mensaje de dibujo ICM notifica a un controlador de representación que descomprima un fotograma de datos y lo dibuje en la pantalla.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- Mensaje de ICM_DRAW de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802029"
---
# <a name="icm_draw-message"></a>Mensaje de dibujo de ICM \_

El mensaje de **\_ dibujo ICM** notifica a un controlador de representación que descomprima un fotograma de datos y lo dibuje en la pantalla.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Puntero a una estructura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si la \_ marca de actualización ICDRAW se establece en el miembro **DwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), el área de la pantalla que se usa para dibujar no es válida y debe actualizarse. La extensión de la actualización depende del contenido del miembro **lpData** .

Si **lpData** es **null**, el controlador debe actualizar el rectángulo de destino completo con la imagen actual. Si el controlador mantiene una copia de la imagen en un búfer fuera de pantalla, puede producir un error en este mensaje. Si **lpData** no es **null**, el controlador debe dibujar los datos y asegurarse de que se actualiza todo el destino.

Si la \_ marca ICDRAW HURRYUP se establece en **dwFlags**, la aplicación que realiza la llamada quiere que el controlador continúe lo más rápido posible, incluso aunque no actualice la pantalla.

Si \_ se establece la marca de preinstalación de ICDRAW en **dwFlags**, este fotograma de vídeo es información preliminar y no se debe mostrar si es posible. Por ejemplo, si Play es empezar desde el fotograma 10 y el fotograma 0 es el fotograma clave anterior, los fotogramas del 0 al 9 tendrán establecido el preICDRAW \_ .

Si desea que el controlador Descomprima los datos en un búfer, envíe el mensaje de [**\_ descompresión ICM**](icm-decompress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





