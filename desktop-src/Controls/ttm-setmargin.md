---
title: TTM_SETMARGIN mensaje (Commctrl.h)
description: Establece los márgenes superior, izquierdo, inferior y derecho de una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5792b33f7f9f5a997759ba390c1b8a713308f95c4ba3f7b5cd0460747ff62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914065"
---
# <a name="ttm_setmargin-message"></a>Mensaje \_ SETMARGIN de TTM

Establece los márgenes superior, izquierdo, inferior y derecho de una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene la información de margen que se va a establecer. Los miembros de la **estructura RECT** no definen un rectángulo delimitador. Para este mensaje, los miembros de la estructura se interpretan de la siguiente manera:



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

Este mensaje no tiene ningún efecto cuando la aplicación se ejecuta en Windows vista y los estilos visuales están habilitados para la información sobre herramientas. Puede deshabilitar los estilos visuales de la información sobre herramientas mediante [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GETMARGIN DE TTM \_**](ttm-getmargin.md)
</dt> </dl>

 

