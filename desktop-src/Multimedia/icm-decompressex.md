---
title: ICM_DECOMPRESSEX mensaje (Vfw.h)
description: El ICM de DECOMPRESSEX notifica a un controlador de compresión de vídeo que descomprima un fotograma de datos directamente en la pantalla, descomprime en una DIB al revés o descomprime imágenes descritas con rectángulos de origen y \_ destino.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370508"
---
# <a name="icm_decompressex-message"></a>\_ICM Mensaje DECOMPRESSEX

El **ICM \_ de DECOMPRESSEX** notifica a un controlador de compresión de vídeo que descomprima un fotograma de datos directamente en la pantalla, descomprime en una DIB al revés o descomprime imágenes descritas con rectángulos de origen y destino.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una [**estructura ICDECOMPRESSEX.**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es similar a [**ICM \_ DECOMPRESS,**](icm-decompress.md) salvo que usa la [**estructura ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir su información de descompresión.

Si desea que el controlador descomprima los datos directamente en la pantalla, envíe el [**ICM \_ DRAW.**](icm-draw.md)

El controlador devuelve un error si este mensaje se recibe antes ICM mensaje [**\_ BEGIN de DECOMPRESSEX. \_**](icm-decompressex-begin.md)

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

 

 





