---
title: Evento External.OnViewChange
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El evento OnViewChange se produce cuando la vista cambia en Reproductor de Windows Media.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Evento External.OnViewChange Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241886"
---
# <a name="externalonviewchange-event"></a>Evento External.OnViewChange

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **evento OnViewChange** se produce cuando la vista cambia en Reproductor de Windows Media.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valores posibles

Se trata de una propiedad de solo escritura que especifica el nombre de la función en el script que Reproductor de Windows Media cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este evento no toma ningún parámetro.

## <a name="remarks"></a>Observaciones

La vista de Reproductor de Windows Media puede cambiar por cualquiera de los siguientes motivos:

-   El usuario interactúa con la interfaz Reproductor de Windows Media usuario.
-   El usuario interactúa con una página de detección y el script de la página de detección llama a [External.changeView](external-changeview.md).
-   El usuario interactúa con una página de detección y el script de la página de detección llama a [External.changeViewOnlineList](external-changeviewonlinelist.md).

Cuando la vista cambia en Reproductor de Windows Media, el reproductor llama a [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) para obtener la dirección URL de la siguiente página de detección que se mostrará. Sin embargo, antes de que player muestre la nueva página de detección, genera el **evento OnViewChange.** Si el controlador de eventos **OnViewChange** llama a [External.cancelNavigate,](external-cancelnavigate.md)Reproductor de Windows Media muestra la nueva página de detección. En su lugar, sigue mostrando la página de detección actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





