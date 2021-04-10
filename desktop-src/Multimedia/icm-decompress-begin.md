---
title: Mensaje de ICM_DECOMPRESS_BEGIN (VFW. h)
description: El \_ mensaje de \_ Inicio de descompresión ICM informa a un controlador de descompresión de vídeo para preparar la descomprimición de los datos. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Mensaje de ICM_DECOMPRESS_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150871"
---
# <a name="icm_decompress_begin-message"></a>\_Mensaje de inicio de descompresión ICM \_

El mensaje de **\_ \_ Inicio** de descompresión ICM informa a un controlador de descompresión de vídeo para preparar la descomprimición de los datos. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


```C++
ICM_DECOMPRESS_BEGIN 
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

Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando el controlador recibe este mensaje, debe asignar búferes y realizar operaciones que consumen mucho tiempo para que pueda procesar los mensajes de [**\_ descomprimir ICM**](icm-decompress.md) de forma eficaz.

Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .

Los mensajes de **\_ \_ Inicio de descompresión de ICM** y [**\_ \_ fin de descompresión ICM**](icm-decompress-end.md) no se anidan. Si el controlador recibe **el \_ \_ Inicio** de la descompresión ICM antes de que se detenga la descompresión con el **\_ \_ fin de descomprimir ICM**, debe reiniciar la descompresión con nuevos parámetros.

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

 

