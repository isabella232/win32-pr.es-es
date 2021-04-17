---
title: External. changeViewOnlineList (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. changeViewOnlineList (método)
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- método changeViewOnlineList de Windows Media Player
- método changeViewOnlineList de Windows Media Player, clase externa
- Clase externa Windows Media Player, método changeViewOnlineList
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
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700026"
---
# <a name="externalchangeviewonlinelist-method"></a>External. changeViewOnlineList (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **changeViewOnlineList** cambia la vista en Windows Media Player para mostrar una lista generada dinámicamente por la tienda en línea.

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

*LibraryLocationType* \[ de\]
</dt> <dd>

Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de la nueva vista. Por ejemplo, la constante CPGenreID especifica que la nueva vista mostrará un género determinado.

</dd> <dt>

*LibraryLocationID* \[ de\]
</dt> <dd>

**Cadena** que contiene el identificador del elemento específico que se va a mostrar en la nueva vista. Por ejemplo, si *LibraryLocationType* es CPGenreID, este parámetro especifica el identificador del género que se va a mostrar en la nueva vista. Esta cadena puede estar vacía.

</dd> <dt>

*Parámetros* \[ de\]
</dt> <dd>

**Cadena** que contiene los parámetros que Windows Media Player pasa al complemento de la tienda en línea mediante una llamada a [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate). Estos parámetros no son interpretados por Media Player de Windows. Los crea la tienda en línea y solo tienen significado en la tienda en línea. Esta cadena puede estar vacía

</dd> <dt>

*FriendlyName* \[ de\]
</dt> <dd>

**Cadena** que contiene un nombre descriptivo que se mostrará en Windows Media Player para la lista dinámica.

</dd> <dt>

*ListType* \[ de\]
</dt> <dd>

Una constante de ubicación de biblioteca que especifica el tipo de los elementos de la lista generada dinámicamente. Por ejemplo, si el valor de este parámetro es CPTrackID, la lista dinámica contendrá pistas.

</dd> <dt>

*ViewMode* \[ de\]
</dt> <dd>

**Cadena** que especifica el modo que Windows Media Player usará para mostrar la lista dinámica. El autor de la llamada debe establecer este parámetro en uno de los valores siguientes, que se definen en contentpartner. h:

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando el script de una página de detección llama a **changeViewOnlineList**, Windows Media Player pasa algunos de los parámetros a los métodos [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) y [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , que se implementan mediante el complemento de la tienda en línea. En la tabla siguiente se muestra la correspondencia entre los parámetros de los tres métodos.



| parámetro changeViewOnlineList | Parámetro GetListContents | Parámetro GetTemplate |
|--------------------------------|---------------------------|-----------------------|
| *LocationType (*                 | *ubicación*                | *ubicación*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *ListType*                     | *bstrListType*            | no aplicable        |



 

Dado que los tres métodos que se muestran en la tabla anterior se implementan en la tienda en línea, tiene cierta flexibilidad en la forma de usar los parámetros. La idea es que proporcione información suficiente para **GetListContents** con el fin de determinar qué lista debe recuperar y **GetTemplate** para determinar qué página de detección debe mostrarse a continuación. En los siguientes ejemplos se muestran dos posibilidades.

**Ejemplo 1: una lista dinámica que está en el catálogo de la tienda en línea**

Supongamos que desea que el complemento obtenga el contenido de la lista dinámica que tiene un identificador de 6 en el catálogo de la tienda en línea. Supongamos que la lista 6 es una lista de pistas. Puede proporcionar suficiente información al complemento realizando la siguiente llamada.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Tenga en cuenta que el parámetro *params* está vacío; el complemento tiene suficiente información en los otros parámetros.

**Ejemplo 2: lista dinámica que no está en el catálogo de la tienda en línea**

Supongamos que desea que el complemento obtenga el contenido de una lista dinámica que no está en el catálogo de la tienda en línea. Es posible que haya decidido tener una lista dinámica que incluye canciones recogidas por un intérprete determinado. Supongamos que el artista tiene un identificador de 2 en el catálogo de la tienda en línea. Podría hacer la siguiente llamada.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Tenga en cuenta que los parámetros *LocationType (* y *LocationID* no especifican la lista. En su lugar, el parámetro *params* especifica la lista. Los parámetros *LocationType (* y *LocationID* se pasan a **IWMPContentPartner:: GetListContents**, pero en este caso, **GetListContents** pueden omitirlos. Los parámetros *LocationType (* y *LocationID* también se pasan a **IWMPContentPartner:: GetTemplate**, que puede usarlos para determinar qué página de detección debe mostrarse con la lista dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





