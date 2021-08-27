---
title: TVN_ASYNCDRAW de notificación (Commctrl.h)
description: Enviado por un control de vista de árbol a su elemento primario cuando se ha dado error en el dibujo de un icono o superposición. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4d929977e1a14a5ada96232fa054c2689d27f1eaa026b64c974d51f5a2c38c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060105"
---
# <a name="tvn_asyncdraw-notification-code"></a>Código de notificación de TVN \_ ASYNCDRAW

Enviado por un control de vista de árbol a su elemento primario cuando se ha dado error en el dibujo de un icono o superposición. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVASYNCDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) La **estructura NMTVASYNCDRAW** contiene la razón por la que se ha generado un error en el dibujo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El control de vista de árbol debe tener el estilo [**\_ extendido TVS EX \_ DRAWIMAGEASYNC.**](tree-view-control-window-extended-styles.md) Tenga en cuenta que esto equivale a la marca LVN ASYNCDRAWN de la vista de lista \_ y su estilo correspondiente.

Este control no se dibuja de forma asincrónica. Asincrónico se usa en el contexto en el que el control de vista de árbol no extrae sincrónicamente una imagen si no está disponible. (Por ejemplo, es posible que la imagen no esté disponible si el control de vista de árbol usa una lista de imágenes dispersas, ya que la imagen se puede descargar). En su lugar, cuando una imagen no está disponible, el control pregunta sincrónicamente al elemento primario qué acción realizar mediante el envío del elemento primario a una notificación ASYNCDRAW de TVN con una estructura \_ [**NMTVASYNCDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) El **miembro hr** de esta estructura describe la razón por la que se ha podido dibujar el control. Un **resultado hr** de E PENDING significa que la imagen no está presente en absoluto \_ (es necesario extraer la imagen). Correcto indica que la imagen está presente, pero no con la calidad de imagen necesaria.

El elemento primario establece el **miembro dwRetFlags** de la estructura para informar al control de cómo continuar. Por ejemplo, el elemento primario puede devolver otra imagen, en el **miembro iRetImageIndex,** para que el control se dibuje. En este caso, el elemento primario establece el **miembro dwRetFlags** en ADRF \_ DRAWIMAGE. Si el control encuentra que no se ha extraído la imagen devuelta, el control puede enviar otra notificación \_ ASYNCDRAW de TVN.

Si una imagen no está disponible, la idea detrás de la asincrónica es permitir que el elemento primario realice la extracción en segundo plano para que la extracción no bloquee el subproceso de interfaz de usuario, es decir, el subproceso en el que está el control. El elemento primario puede devolver ADRF \_ DRAWNOTHING al control y, a continuación, iniciar un subproceso en segundo plano para extraer el icono. Una vez extraído, el elemento primario puede establecer el icono en el control treeview con la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem). Esto hace que la vista de árbol invalide el elemento y, finalmente, vuelva a dibujarlo con la imagen extraída en la lista de imágenes.

En el ejemplo de código siguiente, que se usará como parte de un programa mayor, se muestra cómo un elemento primario puede procesar dos códigos de retorno posibles en esta notificación por un control y decidir qué acción debe realizar el control. No **se muestra el valor dwRetFlags.**


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





