---
title: Mensaje de ICM_COMPRESS_BEGIN (VFW. h)
description: El mensaje de inicio de compress de ICM \_ notifica a \_ un controlador de compresión de vídeo que debe prepararse para comprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- Mensaje de ICM_COMPRESS_BEGIN de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079752"
---
# <a name="icm_compress_begin-message"></a>Mensaje de inicio de \_ compresión ICM \_

El mensaje de **\_ \_ Inicio de compress de ICM** notifica a un controlador de compresión de vídeo que debe prepararse para comprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


```C++
ICM_COMPRESS_BEGIN 
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

Devuelve ICERR \_ OK si el controlador admite la compresión especificada o \_ BADFORMAT ICERR si no se admite el formato de entrada o salida.

## <a name="remarks"></a>Observaciones

El controlador debe asignar e inicializar las tablas o la memoria que necesita para comprimir los formatos de datos cuando recibe el mensaje [**de \_ compresión ICM**](icm-compress.md) .

VCM guarda la configuración del mensaje de **Inicio de \_ compresión \_ ICM** más reciente. Los mensajes end **\_ compress \_ Begin** y [**ICM \_ compress \_**](icm-compress-end.md) no se anidan. Si el controlador recibe la compresión de **ICM \_ \_ comienza** antes de que se detenga la compresión con el **\_ \_ fin de comprimir ICM**, debe reiniciar la compresión con nuevos parámetros.

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

 

