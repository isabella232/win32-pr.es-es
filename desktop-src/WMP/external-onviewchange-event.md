---
title: Evento external. OnViewChange
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El evento OnViewChange se produce cuando cambia la vista en Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Media Player de eventos external. OnViewChange de Windows
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698586"
---
# <a name="externalonviewchange-event"></a>Evento external. OnViewChange

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El evento **OnViewChange** se produce cuando cambia la vista en Windows Media Player.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Observaciones

La vista de Windows Media Player puede cambiar por cualquiera de los siguientes motivos:

-   El usuario interactúa con la interfaz de usuario de Media Player de Windows.
-   El usuario interactúa con una página de detección y el script en la página de detección llama a [external. changeView](external-changeview.md).
-   El usuario interactúa con una página de detección y el script en la página de detección llama a [external. changeViewOnlineList](external-changeviewonlinelist.md).

Cuando la vista cambia en Windows Media Player, el reproductor llama a [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) para obtener la dirección URL de la página de detección siguiente que se va a mostrar. Sin embargo, antes de que el reproductor muestre la nueva página de detección, se genera el evento **OnViewChange** . Si el controlador de eventos **OnViewChange** llama a [external. cancelNavigate](external-cancelnavigate.md), Windows Media Player no muestra la nueva página de detección. En su lugar, sigue mostrando la página de detección actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





