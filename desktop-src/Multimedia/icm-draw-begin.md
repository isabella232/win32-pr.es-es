---
title: ICM_DRAW_BEGIN mensaje (Vfw.h)
description: El ICM \_ DRAW \_ BEGIN notifica a un controlador de representación que se prepare para dibujar datos.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161413"
---
# <a name="icm_draw_begin-message"></a>\_ICM Draw \_ BEGIN message

El **ICM \_ DRAW \_ BEGIN** notifica a un controlador de representación que se prepare para dibujar datos.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

Puntero a una [**estructura ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) que contiene el formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de **ICDRAWBEGIN.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR OK si el controlador admite dibujar los datos en la pantalla de la manera y el formato especificados, o bien un código de error en caso \_ contrario. Los valores de error posibles incluyen lo siguiente.



| Value               | Significado                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ BADFORMAT    | No se admite el formato de entrada o salida.                                      |
| ICERR \_ NO COMPATIBLE | El controlador no dibuja directamente en la pantalla o no admite este mensaje. |



 

## <a name="remarks"></a>Observaciones

Si desea que el controlador descomprima los datos en un búfer, envíe el [**ICM \_ BEGIN de DECOMPRESS. \_**](icm-decompress-begin.md)

Los **ICM \_ DRAW \_ BEGIN** [**y ICM \_ DRAW \_ END**](icm-draw-end.md) no anidan. Si el controlador recibe **ICM \_ DRAW \_ BEGIN** antes de detener la descompresión con **ICM DRAW \_ \_ END,** debe reiniciar la descompresión con nuevos parámetros.

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

 

 





