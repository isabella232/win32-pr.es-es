---
title: Evento External.OnLoginChange
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Evento External.OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Evento External.OnLoginChange Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0697aff759309bc3a988e6f24a024d5c05bd8ec27dae85921ee09d3847f3dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648745"
---
# <a name="externalonloginchange-event"></a>Evento External.OnLoginChange

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **evento OnLoginChange** se produce cuando cambia el estado de inicio de sesión del usuario o cuando se produce un error al intentar iniciar sesión.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Se trata de una propiedad de solo escritura que especifica el nombre de la función en el script que Reproductor de Windows Media cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Comentarios

Este evento se produce cada vez que el complemento de la tienda en línea llama a [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro *de* tipo. A veces, el complemento realiza esta llamada para notificar a Reproductor de Windows Media que se ha registrado un cambio en el estado de inicio de sesión del usuario. Otras veces, el complemento realiza esta llamada para notificar al reproductor que se ha produce un error al intentar iniciar sesión. El *parámetro pContext* del método **Notify** especifica si la notificación es para un cambio de estado de inicio de sesión o para un intento de inicio de sesión con errores.

Dado que cada llamada a hace que Reproductor de Windows Media genera el evento `Notify(wmpcnLoginStateChange, ...)` **OnLoginChange,** a veces se llama al controlador de eventos **OnLoginChange** como resultado de un cambio en el estado de inicio de sesión y, a veces, como resultado de un intento de inicio de sesión con errores. Para determinar el estado de inicio de sesión actual del usuario, el controlador de eventos **OnLoginChange** debe llamar a [External.userLoggedIn](external-userloggedin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





