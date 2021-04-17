---
title: Mensaje de ICM_COMPRESS_QUERY (VFW. h)
description: El mensaje de consulta de compresión ICM consulta \_ \_ un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede comprimir un formato de entrada específico a un formato de salida específico.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- Mensaje de ICM_COMPRESS_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676900"
---
# <a name="icm_compress_query-message"></a>Mensaje de consulta de \_ compresión ICM \_

El mensaje de **\_ \_ consulta** de compresión ICM consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede comprimir un formato de entrada específico a un formato de salida específico. Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .


```C++
ICM_COMPRESS_QUERY 
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

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida. Puede especificar cero para que este parámetro indique que el formato de salida es aceptable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se admite la compresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando un controlador recibe este mensaje, debe examinar la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) asociada a *lpbiInput* para determinar si puede comprimir el formato de entrada.

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

 

