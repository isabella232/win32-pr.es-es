---
title: Evento external. OnLoginChange
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Media Player de eventos external. OnLoginChange de Windows
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
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698590"
---
# <a name="externalonloginchange-event"></a>Evento external. OnLoginChange

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El evento **OnLoginChange** se produce cuando cambia el estado del inicio de sesión del usuario o cuando se produce un error al intentar iniciar sesión.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Observaciones

Este evento se produce cada vez que el complemento de la tienda en línea llama a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro de *tipo* . A veces, el complemento realiza esta llamada para notificar a Windows Media Player que se ha producido un cambio en el estado de inicio de sesión del usuario. En otras ocasiones, el complemento realiza esta llamada para notificar al reproductor que se produjo un error al intentar iniciar sesión. El parámetro *pContext* del método **Notify** especifica si la notificación es para un cambio de estado de inicio de sesión o para un intento de inicio de sesión erróneo.

Dado que cada llamada a `Notify(wmpcnLoginStateChange, ...)` hace que Windows Media Player genere el evento **OnLoginChange** , a veces se llama al controlador de eventos **OnLoginChange** como resultado de un cambio en el estado de inicio de sesión y, a veces, como resultado de un intento de inicio de sesión erróneo. Para determinar el estado de inicio de sesión actual del usuario, el controlador de eventos **OnLoginChange** debe llamar a [external. userLoggedIn](external-userloggedin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





