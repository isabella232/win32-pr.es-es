---
title: Mensaje de ICM_DECOMPRESSEX (VFW. h)
description: El \_ mensaje DECOMPRESSEX de ICM notifica a un controlador de compresión de vídeo que debe descomprimir un fotograma de datos directamente en la pantalla, descomprimir en un DIB en paralelo o descomprimir imágenes que se describen con los rectángulos de origen y de destino.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Mensaje de ICM_DECOMPRESSEX de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079641"
---
# <a name="icm_decompressex-message"></a>\_Mensaje DECOMPRESSEX ICM

El **mensaje \_ DECOMPRESSEX de ICM** notifica a un controlador de compresión de vídeo que debe descomprimir un fotograma de datos directamente en la pantalla, descomprimir en un DIB en paralelo o descomprimir imágenes que se describen con los rectángulos de origen y de destino.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje es similar a la descompresión de ICM, con la diferencia de que usa la estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir la información de descompresión. [**\_**](icm-decompress.md)

Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .

El controlador devuelve un error si este mensaje se recibe antes del mensaje de [**\_ \_ Inicio DECOMPRESSEX de ICM**](icm-decompressex-begin.md) .

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

 

 





