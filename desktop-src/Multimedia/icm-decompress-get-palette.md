---
title: ICM_DECOMPRESS_GET_PALETTE mensaje (Vfw.h)
description: El ICM mensaje GET PALETTE de DECOMPRESS solicita que el controlador de descompresión de vídeo proporcione la tabla de colores de la estructura \_ \_ \_ BITMAPINFOHEADER de salida. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370531"
---
# <a name="icm_decompress_get_palette-message"></a>\_ICM MENSAJE GET PALETTE DE DECOMPRESS \_ \_

El ICM mensaje GET PALETTE de **\_ DECOMPRESS \_ \_** solicita que el controlador de descompresión de vídeo proporcione la tabla de colores de la estructura [**BITMAPINFOHEADER de**](/previous-versions//dd183376(v=vs.85)) salida. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette)


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contiene el formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contiene la tabla de colores. El espacio reservado para la tabla de colores siempre es de al menos 256 colores. Puede especificar cero para que este parámetro devuelva solo el tamaño de la tabla de colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si *lpbiOutput* es distinto de cero, el controlador establece el miembro **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) en el número de colores de la tabla de colores. El controlador rellena el **miembro bmiColors** de [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con los colores reales.

El controlador solo debe admitir este mensaje si usa una paleta que no sea la especificada en el formato de entrada.

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

 

