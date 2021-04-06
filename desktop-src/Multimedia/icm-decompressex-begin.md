---
title: Mensaje de ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: El \_ mensaje de inicio DECOMPRESSEX de ICM notifica a \_ un controlador de compresión de vídeo que debe prepararse para descomprimir los datos.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Mensaje de ICM_DECOMPRESSEX_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803367"
---
# <a name="icm_decompressex_begin-message"></a>Mensaje de inicio de \_ DECOMPRESSEX ICM \_

El mensaje de **\_ \_ Inicio DECOMPRESSEX de ICM** notifica a un controlador de compresión de vídeo que debe prepararse para descomprimir los datos.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene los formatos de entrada y salida.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando el controlador recibe este mensaje, debe asignar búferes y realizar operaciones que consumen mucho tiempo para que pueda procesar los [**mensajes \_ DECOMPRESSEX ICM**](icm-decompressex.md) de forma eficaz.

Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) .

Los mensajes de [**\_ \_ finalización**](icm-decompressex-end.md) de **DECOMPRESSEX de ICM \_ \_** y de fin de DECOMPRESSEX no se anidan. Si el controlador recibe **el \_ \_ Inicio de DECOMPRESSEX ICM** antes de que se detenga la descompresión con **ICM \_ DECOMPRESSEX \_ End**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





