---
title: ICM_COMPRESS_BEGIN mensaje (Vfw.h)
description: El ICM \_ COMPRESS \_ BEGIN notifica a un controlador de compresión de vídeo que se prepare para comprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062908"
---
# <a name="icm_compress_begin-message"></a>\_ICM Mensaje \_ COMPRESS BEGIN

El **ICM \_ COMPRESS \_ BEGIN** notifica a un controlador de compresión de vídeo que se prepare para comprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressBegin.**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin)


```C++
ICM_COMPRESS_BEGIN 
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

Devuelve ICERR OK si el controlador admite la compresión especificada o ICERR BADFORMAT si no se admite el formato de entrada \_ \_ o salida.

## <a name="remarks"></a>Observaciones

El controlador debe asignar e inicializar las tablas o memoria que necesite para comprimir los formatos de datos cuando recibe el [**ICM \_ COMPRESS.**](icm-compress.md)

VCM guarda la configuración de la versión más **reciente ICM el mensaje COMPRESS \_ \_ BEGIN.** Los **ICM LOS MENSAJES BEGIN y COMPRESS \_ \_ BEGIN** [**ICM los mensajes COMPRESS \_ \_ END**](icm-compress-end.md) no se anidan. Si el controlador recibe ICM **\_ COMPRESS \_ BEGIN** antes de detener la compresión con **ICM COMPRESS \_ \_ END,** debe reiniciar la compresión con nuevos parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

