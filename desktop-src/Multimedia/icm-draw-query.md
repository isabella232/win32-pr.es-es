---
title: ICM_DRAW_QUERY mensaje (Vfw.h)
description: El ICM DRAW QUERY consulta a un controlador de representación para determinar si \_ puede representar datos en un formato \_ específico. Puede enviar este mensaje explícitamente o mediante la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370550"
---
# <a name="icm_draw_query-message"></a>\_ICM Draw \_ QUERY message

El **ICM draw query \_ \_ consulta** consulta a un controlador de representación para determinar si puede representar los datos en un formato específico. Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery)


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntero a una [**estructura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ICERR OK si el controlador puede representar los datos en el formato especificado o \_ ICERR BADFORMAT en caso \_ contrario.

## <a name="remarks"></a>Observaciones

Este mensaje difiere del ICM [**\_ DRAW \_ BEGIN**](icm-draw-begin.md) en que consulta el controlador en un sentido general. **ICM \_ DRAW \_ BEGIN** determina si el controlador puede dibujar los datos con el formato especificado en condiciones específicas, como extender la imagen.

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

 

