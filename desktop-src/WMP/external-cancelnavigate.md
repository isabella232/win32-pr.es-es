---
title: External. cancelNavigate (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. cancelNavigate (método)
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- método cancelNavigate de Windows Media Player
- método cancelNavigate de Windows Media Player, clase externa
- Clase externa Windows Media Player, método cancelNavigate
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
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700030"
---
# <a name="externalcancelnavigate-method"></a>External. cancelNavigate (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **cancelNavigate** informa a Windows Media Player que no debe mostrar una nueva página de detección aunque la vista haya cambiado en el reproductor.

## <a name="syntax"></a>Sintaxis


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando la vista cambia en Windows Media Player, el reproductor llama al complemento de la tienda en línea para determinar la página de detección que se va a mostrar a continuación. En algunos casos, sin embargo, la tienda en línea podría querer que el reproductor continuara mostrando la página de detección existente. El siguiente proceso determina si el reproductor muestra una nueva página de detección:

1.  Una acción por parte del usuario, ya sea en la interfaz de usuario del reproductor o en la página de detección, solicita que el reproductor cambie su vista.
2.  El reproductor llama al método [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del complemento para determinar qué página de detección se va a mostrar a continuación. El reproductor almacena la dirección URL de la nueva página de detección, pero no muestra la nueva página de detección en este momento.
3.  El reproductor genera el evento [OnViewChange](external-onviewchange-event.md) .
4.  Si el controlador de eventos **OnViewChange** de la página de detección llama a **CancelNavigate**, el reproductor no muestra la nueva página de detección (determinada en el paso 2). En su lugar, sigue mostrando la página de detección existente. Si el controlador de eventos **OnViewChange** no llama a **CancelNavigate**, el reproductor muestra la nueva página de detección.

Por ejemplo, supongamos que el reproductor muestra actualmente la vista de un álbum con una determinada pista seleccionada. Supongamos también que la página de detección actual es la página que representa el álbum completo. Si el usuario hace clic en otra pista del mismo álbum, la vista del jugador cambia ligeramente para mostrar que la nueva pista está seleccionada. Sin embargo, no es necesario mostrar una nueva página de detección. La página de detección que representa el álbum completo sigue siendo la página adecuada para que la muestre el reproductor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





