---
title: Evento External.OnChangeViewOnlineListError
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Evento External.OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Evento External.OnChangeViewOnlineListError Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ed6191de129bffea0e11abb24f1e271fc0b2873d2b306430a4e7eafe39b214d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648805"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Evento External.OnChangeViewOnlineListError

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **evento OnChangeViewOnlineListError** se produce cuando una llamada al [método External.changeViewOnlineList](external-changeviewonlinelist.md) produce un error.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Valores posibles

Se trata de una propiedad de solo escritura que especifica el nombre de la función en el script que Reproductor de Windows Media cuando se produce el evento.

## <a name="parameters"></a>Parámetros

La función que controla este error tiene los parámetros siguientes.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Código **de error HRESULT** que indica el motivo del error.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La misma cadena que se pasó en el **parámetro LibraryLocationType** **de changeViewOnlineList.**

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La misma cadena que se pasó en el **parámetro LibraryLocationID** **de changeViewOnlineList**.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

La misma cadena que se pasó en el parámetro **Params** **de changeViewOnlineList.**

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*
</dt> <dd>

La misma cadena que se pasó en el **parámetro FriendlyName** **de changeViewOnlineList**.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

La misma cadena que se pasó en el **parámetro ListType** **de changeViewOnlineList**.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*Viewmode*
</dt> <dd>

La misma cadena que se pasó en el **parámetro ViewMode** **de changeViewOnlineList**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





