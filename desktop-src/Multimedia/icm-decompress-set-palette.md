---
title: Mensaje de ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: El \_ mensaje de decompredor de la \_ paleta Set ICM \_ especifica una paleta para que un controlador de descompresión de vídeo lo use si se está descomprime con un formato que usa una paleta. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Mensaje de ICM_DECOMPRESS_SET_PALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676893"
---
# <a name="icm_decompress_set_palette-message"></a>Descompresor ICM \_ \_ set \_ Palette Message

El mensaje de **\_ decompredor de la \_ \_ paleta Set ICM** especifica una paleta para que un controlador de descompresión de vídeo lo use si se está descomprime con un formato que usa una paleta. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Puntero a una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) cuya tabla de colores contiene los colores que se deben usar si es posible. Puede especificar cero para usar el conjunto predeterminado de colores de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador de descompresión puede descomprimir imágenes con precisión en la paleta sugerida mediante el conjunto de colores que se organizan en la paleta. Devuelve ICERR \_ no compatible en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje no debe afectar a la descompresión que ya está en curso; en su lugar, se deben devolver los colores que se pasan con este mensaje en respuesta a los mensajes de la paleta [**de obtención y \_ \_ \_**](icm-decompress-get-format.md) [**\_ descompresión \_ \_ ICM**](icm-decompress-get-palette.md) más adelante. Los colores se devuelven al controlador de descompresión en un futuro mensaje de [**\_ \_ Inicio descomprimido de ICM**](icm-decompress-begin.md) .

Este mensaje se utiliza principalmente cuando un controlador descomprime imágenes en la pantalla y otra aplicación que usa una paleta está en primer plano, lo que obliga al controlador de descompresión a adaptarse a un conjunto de colores externo.

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

 

