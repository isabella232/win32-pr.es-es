---
title: Mensaje de ICM_DECOMPRESS (VFW. h)
description: El \_ mensaje de descompresión ICM informa a un controlador de descompresión de vídeo para descomprimir un marco de datos en un búfer definido por la aplicación.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- Mensaje de ICM_DECOMPRESS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079642"
---
# <a name="icm_decompress-message"></a>Descompresión de ICM \_

El mensaje de descompresión **ICM \_** informa a un controlador de descompresión de vídeo para descomprimir un marco de datos en un búfer definido por la aplicación.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*ICD*
</dt> <dd>

Puntero a una estructura [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .

El controlador devuelve un error si este mensaje se recibe antes del mensaje de [**\_ \_ Inicio de descompresión de ICM**](icm-decompress-begin.md) .

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

 

 





