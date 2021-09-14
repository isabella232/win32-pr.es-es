---
title: ICM_DECOMPRESS mensaje (Vfw.h)
description: El ICM mensaje DECOMPRESS notifica a un controlador de descompresión de vídeo que descomprima un marco de datos en un búfer definido \_ por la aplicación.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074226"
---
# <a name="icm_decompress-message"></a>\_ICM Mensaje DECOMPRESS

El **ICM \_ de DECOMPRESS** notifica a un controlador de descompresión de vídeo que descomprima un marco de datos en un búfer definido por la aplicación.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*Icd*
</dt> <dd>

Puntero a una [**estructura ICDECOMPRESS.**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si desea que el controlador descomprima los datos directamente en la pantalla, envíe el [**ICM \_ DRAW.**](icm-draw.md)

El controlador devuelve un error si este mensaje se recibe antes ICM [**\_ mensaje DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

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

 

 





