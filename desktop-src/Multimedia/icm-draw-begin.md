---
title: Mensaje de ICM_DRAW_BEGIN (VFW. h)
description: El mensaje de inicio de Draw de ICM \_ notifica a \_ un controlador de representación que debe prepararse para dibujar los datos.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Mensaje de ICM_DRAW_BEGIN de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996895"
---
# <a name="icm_draw_begin-message"></a>Mensaje de inicio de \_ dibujo ICM \_

El mensaje de **\_ \_ Inicio de Draw de ICM** notifica a un controlador de representación que debe prepararse para dibujar los datos.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

Puntero a una estructura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) que contiene el formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamaño, en bytes, de **ICDRAWBEGIN**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador permite dibujar los datos en la pantalla de la forma y el formato especificados, o un código de error en caso contrario. Entre los posibles valores de error se incluyen los siguientes.



| Value               | Significado                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ BADFORMAT    | No se admite el formato de entrada o salida.                                      |
| ICERR \_ NOTSUPPORTED | El controlador no dibuja directamente en la pantalla o no admite este mensaje. |



 

## <a name="remarks"></a>Observaciones

Si desea que el controlador Descomprima los datos en un búfer, envíe el mensaje de [**\_ \_ Inicio de descompresión ICM**](icm-decompress-begin.md) .

Los mensajes de **\_ \_ Inicio de dibujo de ICM** y [**\_ \_ fin de dibujo de ICM**](icm-draw-end.md) no se anidan. Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la descompresión con el **\_ \_ extremo de Draw ICM**, debe reiniciar la descompresión con nuevos parámetros.

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

 

 





