---
title: Mensaje de ICM_DRAW_QUERY (VFW. h)
description: El mensaje de consulta de dibujo de ICM consulta \_ \_ un controlador de representación para determinar si puede representar datos en un formato específico. Puede enviar este mensaje explícitamente o mediante la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Mensaje de ICM_DRAW_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491147"
---
# <a name="icm_draw_query-message"></a>Mensaje de consulta de \_ Draw ICM \_

El mensaje de **\_ \_ consulta de dibujo de ICM** consulta un controlador de representación para determinar si puede representar datos en un formato específico. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR \_ OK si el controlador puede representar datos en el formato especificado o ICERR \_ BADFORMAT de lo contrario.

## <a name="remarks"></a>Observaciones

Este mensaje difiere del mensaje [**de \_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) en que consulta el controlador en un sentido general. **ICM \_ \_Empezar a dibujar** determina si el controlador puede dibujar los datos con el formato especificado en condiciones específicas, como la ampliación de la imagen.

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

 

