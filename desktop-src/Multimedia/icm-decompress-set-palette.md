---
title: ICM_DECOMPRESS_SET_PALETTE mensaje (Vfw.h)
description: El ICM DECOMPRESS SET PALETTE especifica una paleta para un controlador \_ \_ de descompresión de vídeo que se va a usar si se está descomprimiendo en un formato que usa una \_ paleta. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246350"
---
# <a name="icm_decompress_set_palette-message"></a>\_ICM Mensaje DE DECOMPRESS \_ SET \_ PALETTE

El **ICM \_ DECOMPRESS \_ SET \_ PALETTE** especifica una paleta para un controlador de descompresión de vídeo que se va a usar si se está descomprimiendo en un formato que usa una paleta. Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette)


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Puntero a una [**estructura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) cuya tabla de colores contiene los colores que se deben usar si es posible. Puede especificar cero para usar el conjunto predeterminado de colores de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR OK si el controlador \_ de descompresión puede descomprimir imágenes con precisión en la paleta sugerida mediante el conjunto de colores a medida que se organizan en la paleta. Devuelve ICERR \_ UNSUPPORTED en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje no debería afectar a la descompresión ya en curso; en su lugar, los colores que se pasan con este mensaje deben devolverse en respuesta a los ICM [**\_ DECOMPRESS \_ GET \_ FORMAT**](icm-decompress-get-format.md) y ICM [**\_ \_ DECOMPRESS GET \_ PALETTE.**](icm-decompress-get-palette.md) Los colores se envían de nuevo al controlador de descompresión en un futuro [**ICM \_ mensaje DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

Este mensaje se usa principalmente cuando un controlador descomprime imágenes en la pantalla y otra aplicación que usa una paleta está en primer plano, lo que obliga al controlador de descompresión a adaptarse a un conjunto externo de colores.

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

 

