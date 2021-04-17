---
title: Código de notificación de TVN_ASYNCDRAW (commctrl. h)
description: Lo envía un control de vista de árbol a su elemento primario cuando se produce un error en el dibujo de un icono o una superposición. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW controles de código de notificación de Windows
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
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658365"
---
# <a name="tvn_asyncdraw-notification-code"></a>Código de notificación de ASYNCDRAW de TVN \_

Lo envía un control de vista de árbol a su elemento primario cuando se produce un error en el dibujo de un icono o una superposición. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . La estructura **NMTVASYNCDRAW** contiene la razón por la que se produjo un error en Draw.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El control de vista de árbol debe tener el estilo extendido [**TV \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) . Tenga en cuenta que esto es equivalente a la marca de LVN ASYNCDRAWN de la vista de lista \_ y su estilo correspondiente.

Este control no se dibuja de forma asincrónica. Asincrónico se utiliza en el contexto de que el control de vista de árbol no extraiga una imagen de forma sincrónica si no está disponible. (Por ejemplo, es posible que la imagen no esté disponible si el control de vista de árbol usa una lista de imágenes dispersas, ya que se puede descargar la imagen). En su lugar, cuando una imagen no está disponible, el control pide sincrónicamente al elemento primario qué acción debe realizar mediante el envío de una notificación primaria a TVN \_ ASYNCDRAW con una estructura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . El miembro **HR** de esta estructura describe la razón por la que se produjo un error en la traza del control. Un resultado de **HR** de E \_ Pending significa que la imagen no está presente en absoluto (es necesario extraer la imagen). Success indica que la imagen está presente pero no con la calidad de imagen requerida.

El elemento primario establece el miembro **dwRetFlags** de la estructura para informar al control de cómo continuar. Por ejemplo, el elemento primario puede devolver otra imagen, en el miembro **iRetImageIndex** , para que el control dibuje. En este caso, el elemento primario establece el miembro **dwRetFlags** en ADRF \_ DRAWIMAGE. Si el control encuentra la imagen devuelta no se ha extraído, \_ puede que el control envíe otra notificación TVN ASYNCDRAW.

Si una imagen no está disponible, la idea detrás de asincrónica es permitir que el elemento primario realice la extracción en segundo plano para que la extracción no bloquee el subproceso de la interfaz de usuario, es decir, el subproceso en el que se encuentra el control. El elemento primario puede devolver ADRF \_ DRAWNOTHING al control y, a continuación, iniciar un subproceso en segundo plano para extraer el icono. Una vez extraído, el elemento primario puede establecer el icono en el control TreeView con la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem). Esto hace que la vista de árbol invalide el elemento y, finalmente, lo vuelva a dibujar con la imagen extraída en la lista de imágenes.

En el ejemplo de código siguiente, que se va a usar como parte de un programa más grande, se muestra cómo un control primario puede procesar dos posibles códigos de retorno en esta notificación por un control y decidir qué acción debe realizar el control. No se muestra el valor de **dwRetFlags** .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





