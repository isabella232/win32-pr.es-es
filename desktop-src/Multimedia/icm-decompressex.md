---
title: ICM_DECOMPRESSEX mensaje (Vfw.h)
description: El ICM de DECOMPRESSEX notifica a un controlador de compresión de vídeo que descomprima un fotograma de datos directamente en la pantalla, descomprima a una DIB al revés o descomprima imágenes descritas con rectángulos de origen y \_ destino.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074222"
---
# <a name="icm_decompressex-message"></a>\_ICM Mensaje DECOMPRESSEX

El **ICM \_ de DECOMPRESSEX** notifica a un controlador de compresión de vídeo que descomprima un marco de datos directamente en la pantalla, se descomprime en una DIB al revés o descomprime imágenes descritas con rectángulos de origen y destino.


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

Tamaño, en bytes, de [**ICDECOMPRESSEX.**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es similar [**a ICM \_ DECOMPRESS, salvo**](icm-decompress.md) que usa la estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir su información de descompresión.

Si desea que el controlador descomprima los datos directamente en la pantalla, envíe el [**ICM \_ DRAW.**](icm-draw.md)

El controlador devuelve un error si este mensaje se recibe antes del [**ICM \_ DECOMPRESSEX \_ BEGIN.**](icm-decompressex-begin.md)

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

 

 





