---
title: TTM_GETMARGIN mensaje (Commctrl.h)
description: Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN controles de Windows mensaje
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
ms.openlocfilehash: 6af1e7f460ad877c5c562f3a5aa47147a27606c54b9a4334eb8fb7b93716c33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060555"
---
# <a name="ttm_getmargin-message"></a>Mensaje \_ GETMARGIN de TTM

Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibirá la información de margen. Los miembros de la **estructura RECT** no definen un rectángulo delimitador. Para este mensaje, los miembros de la estructura se interpretan de la siguiente manera:



| Value                                                                                                                                   | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | Distancia entre el borde superior y la parte superior del texto de la información sobre herramientas, en píxeles.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Izquierda**</dt> </dl>       | Distancia entre el borde izquierdo y el extremo izquierdo del texto de la información sobre herramientas, en píxeles.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**Parte inferior**</dt> </dl> | Distancia entre el borde inferior y la parte inferior del texto de la información sobre herramientas, en píxeles.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Correcto**</dt> </dl>    | Distancia entre el borde derecho y el extremo derecho del texto de la información sobre herramientas, en píxeles.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Comentarios

Los cuatro márgenes tienen como valor predeterminado cero cuando se crea el control de información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SETMARGIN DE TTM \_**](ttm-setmargin.md)
</dt> </dl>

 

