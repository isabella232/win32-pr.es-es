---
title: Mensaje de TTM_GETMARGIN (commctrl. h)
description: Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996413"
---
# <a name="ttm_getmargin-message"></a>TTM \_ GETMARGIN

Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del margen. Los miembros de la estructura **Rect** no definen un rectángulo delimitador. Para este mensaje, los miembros de la estructura se interpretan de la siguiente manera:



| Value                                                                                                                                   | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Arriba**</dt> </dl>          | Distancia entre el borde superior y la parte superior del texto de información sobre herramientas, en píxeles.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**salido**</dt> </dl>       | Distancia entre el borde izquierdo y el final izquierdo del texto de información sobre herramientas, en píxeles.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**descendente**</dt> </dl> | Distancia entre el borde inferior y la parte inferior del texto de información sobre herramientas, en píxeles.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**correcta**</dt> </dl>    | Distancia entre el borde derecho y el extremo derecho del texto de información sobre herramientas, en píxeles.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Los cuatro márgenes tienen como valor predeterminado cero al crear el control ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TTM \_ SETMARGIN**](ttm-setmargin.md)
</dt> </dl>

 

