---
title: Método External.cancelNavigate
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Método External.cancelNavigate
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Método cancelNavigate Reproductor de Windows Media
- Método cancelNavigate Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media método , cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649435"
---
# <a name="externalcancelnavigate-method"></a>Método External.cancelNavigate

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método cancelNavigate** informa Reproductor de Windows Media que no debe mostrar una nueva página de detección aunque la vista haya cambiado en el reproductor.

## <a name="syntax"></a>Sintaxis


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando la vista cambia en Reproductor de Windows Media, el reproductor llama al complemento de la tienda en línea para determinar qué página de detección se mostrará a continuación. Sin embargo, en algunos casos, es posible que la tienda en línea quiera que el reproductor siga mostrando la página de detección existente. El siguiente proceso determina si el reproductor muestra una nueva página de detección:

1.  Una acción del usuario, ya sea en la interfaz de usuario del reproductor o en la página de detección, solicita que el reproductor cambie su vista.
2.  El reproductor llama al método [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del complemento para determinar qué página de detección se va a mostrar a continuación. El reproductor almacena la dirección URL de la nueva página de detección, pero no muestra la nueva página de detección en este momento.
3.  El reproductor genera el [evento OnViewChange.](external-onviewchange-event.md)
4.  Si el controlador de eventos **OnViewChange** de la página de detección llama a **cancelNavigate**, el reproductor no muestra la nueva página de detección (determinada en el paso 2). En su lugar, sigue mostrando la página de detección existente. Si el **controlador de eventos OnViewChange** no llama a **cancelNavigate,** el reproductor muestra la nueva página de detección.

Por ejemplo, suponga que el reproductor muestra actualmente la vista de un álbum con una pista determinada seleccionada. Supongamos también que la página de detección actual es la página que representa todo el álbum. Si el usuario hace clic en una pista diferente del mismo álbum, la vista del reproductor cambia ligeramente para mostrar que la nueva pista está seleccionada. Pero no es necesario mostrar una nueva página de detección. La página de detección que representa todo el álbum sigue siendo la página adecuada para que la muestre el jugador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





