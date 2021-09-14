---
title: ICM_COMPRESS_GET_SIZE mensaje (Vfw.h)
description: El ICM mensaje COMPRESS GET SIZE solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el \_ \_ formato de salida \_ especificado. Puede enviar este mensaje explícitamente o mediante la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246387"
---
# <a name="icm_compress_get_size-message"></a>\_ICM Mensaje COMPRESS \_ GET \_ SIZE

El **ICM mensaje COMPRESS GET \_ \_ \_ SIZE** solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el formato de salida especificado. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressGetSize.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize)


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número máximo de bytes que puede ocupar un único marco comprimido.

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones envían este mensaje para determinar el tamaño de un búfer que se va a asignar para el marco comprimido.

El controlador debe calcular el tamaño del fotograma más grande posible en función de los formatos de entrada y salida.

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

 

