---
title: Mensaje de ICM_COMPRESS_GET_SIZE (VFW. h)
description: El \_ mensaje comprimir \_ de \_ tamaño del dispositivo Get size solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el formato de salida especificado. Puede enviar este mensaje explícitamente o mediante la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- Mensaje de ICM_COMPRESS_GET_SIZE de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996898"
---
# <a name="icm_compress_get_size-message"></a>\_Mensaje de \_ obtención de tamaño de compresión \_ ICM

El mensaje comprimir de tamaño del dispositivo **\_ \_ Get \_ size** solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el formato de salida especificado. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número máximo de bytes que puede ocupar un solo fotograma comprimido.

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones envían este mensaje para determinar el tamaño de un búfer que se va a asignar al marco comprimido.

El controlador debe calcular el tamaño del fotograma más grande posible en función de los formatos de entrada y salida.

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

 

