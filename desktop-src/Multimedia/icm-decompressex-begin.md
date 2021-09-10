---
title: ICM_DECOMPRESSEX_BEGIN mensaje (Vfw.h)
description: El ICM DECOMPRESSEX BEGIN notifica a un controlador de compresión de vídeo \_ que se prepare para \_ descomprimir los datos.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370513"
---
# <a name="icm_decompressex_begin-message"></a>\_ICM Mensaje BEGIN de \_ DECOMPRESSEX

El **ICM \_ DECOMPRESSEX \_ BEGIN** notifica a un controlador de compresión de vídeo que se prepare para descomprimir los datos.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntero a una [**estructura ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene los formatos de entrada y salida.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando el controlador recibe este mensaje, debe asignar búferes y realizar las operaciones que requieren mucho tiempo para que pueda procesar ICM [**\_ mensajes DECOMPRESSEX**](icm-decompressex.md) de forma eficaz.

Si desea que el controlador descomprima los datos directamente en la pantalla, envíe el [**ICM \_ DRAW \_ BEGIN.**](icm-draw-begin.md)

Los **ICM \_ DECOMPRESSEX \_ BEGIN** y ICM los mensajes [**END de \_ DECOMPRESSEX \_**](icm-decompressex-end.md) no se anidan. Si el controlador recibe ICM **\_ DECOMPRESSEX \_ BEGIN** antes de detener la descompresión con ICM **\_ DECOMPRESSEX \_ END,** debe reiniciar la descompresión con nuevos parámetros.

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

 

 





