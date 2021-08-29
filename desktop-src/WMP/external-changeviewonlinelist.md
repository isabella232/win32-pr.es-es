---
title: Método External.changeViewOnlineList
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Método External.changeViewOnlineList
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- Método changeViewOnlineList Reproductor de Windows Media
- Método changeViewOnlineList Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media método , changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd5601dc1eaa1ad325a39e1a340537c3863eee48f26510acefbc57ecd0cdbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649265"
---
# <a name="externalchangeviewonlinelist-method"></a>Método External.changeViewOnlineList

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método changeViewOnlineList** cambia la vista en Reproductor de Windows Media mostrar una lista generada dinámicamente por la tienda en línea.

## <a name="syntax"></a>Sintaxis


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LibraryLocationType* \[ En\]
</dt> <dd>

Constante [de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de la nueva vista. Por ejemplo, la constante CPGenreID especifica que la nueva vista mostrará un género determinado.

</dd> <dt>

*LibraryLocationID* \[ En\]
</dt> <dd>

**Cadena** que contiene el identificador del elemento específico que se mostrará en la nueva vista. Por ejemplo, si *LibraryLocationType* es CPGenreID, este parámetro especifica el identificador del género que se va a mostrar en la nueva vista. Esta cadena puede estar vacía.

</dd> <dt>

*Params* \[ En\]
</dt> <dd>

**Cadena** que contiene parámetros que Reproductor de Windows Media pasa al complemento de la tienda en línea mediante una llamada a [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate). Estos parámetros no se interpretan mediante Reproductor de Windows Media. Se crean mediante la tienda en línea y solo tienen significado para la tienda en línea. Esta cadena puede estar vacía

</dd> <dt>

*FriendlyName* \[ En\]
</dt> <dd>

**Cadena** que contiene un nombre descriptivo, que se va a mostrar Reproductor de Windows Media, para la lista dinámica.

</dd> <dt>

*ListType* \[ En\]
</dt> <dd>

Constante de ubicación de biblioteca que especifica el tipo de los elementos de la lista generada dinámicamente. Por ejemplo, si el valor de este parámetro es CPTrackID, la lista dinámica contendrá pistas.

</dd> <dt>

*ViewMode* \[ En\]
</dt> <dd>

**Cadena** que especifica el modo que Reproductor de Windows Media usará para mostrar la lista dinámica. El autor de la llamada debe establecer este parámetro en uno de los siguientes valores, que se definen en contentpartner.h:

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando el script de una página de detección llama a **changeViewOnlineList,** Reproductor de Windows Media pasa algunos de los parámetros junto con los métodos [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) e [IWMPContentPartner::GetTemplate,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) que se implementan mediante el complemento de la tienda en línea. En la tabla siguiente se muestra la correspondencia entre los parámetros de los tres métodos.



| parámetro changeViewOnlineList | Parámetro GetListContents | Parámetro GetTemplate |
|--------------------------------|---------------------------|-----------------------|
| *LocationType*                 | *ubicación*                | *ubicación*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *ListType*                     | *bstrListType*            | no aplicable        |



 

Dado que los tres métodos que se muestran en la tabla anterior se implementan mediante la tienda en línea, tiene cierta flexibilidad en la forma de usar los parámetros. La idea es que proporcione suficiente información para **que GetListContents** determine qué lista debe recuperar y para **que GetTemplate** determine qué página de detección se debe mostrar a continuación. En los ejemplos siguientes se muestran dos posibilidades.

**Ejemplo 1: una lista dinámica que se encuentra en el catálogo de la tienda en línea**

Supongamos que quiere que el complemento obtenga el contenido de la lista dinámica que tiene un identificador de 6 en el catálogo de la tienda en línea. Supongamos que la lista 6 es una lista de pistas. Puede proporcionar al complemento suficiente información mediante la realización de la siguiente llamada.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Tenga en cuenta que *el parámetro Params* está vacío; el complemento tiene suficiente información en los demás parámetros.

**Ejemplo 2: Una lista dinámica que no está en el catálogo de la tienda en línea**

Supongamos que quiere que el complemento obtenga el contenido de una lista dinámica que no está en el catálogo de la tienda en línea. Quizás haya decidido tener una lista dinámica que incluya canciones que haya elegido un intérprete determinado. Suponga que el intérprete tiene un identificador de 2 en el catálogo de la tienda en línea. Puede realizar la siguiente llamada.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Tenga en cuenta *que los parámetros LocationType* y *LocationID* no especifican la lista. En su lugar, *el parámetro Params* especifica la lista. Los *parámetros LocationType* y *LocationID* se pasan a **IWMPContentPartner::GetListContents,** pero en este caso, **GetListContents** puede omitirlos. Los *parámetros LocationType* y *LocationID* también se pasan a **IWMPContentPartner::GetTemplate**, que puede usarlos para determinar qué página de detección se debe mostrar con la lista dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





