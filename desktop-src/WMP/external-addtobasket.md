---
title: External. addToBasket (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. addToBasket (método)
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- método addToBasket de Windows Media Player
- método addToBasket de Windows Media Player, clase externa
- Clase externa Windows Media Player, método addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699873"
---
# <a name="externaladdtobasket-method"></a>External. addToBasket (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **addToBasket** agrega elementos multimedia al panel lista (también denominado cesta) en Windows Media Player.

## <a name="syntax"></a>Sintaxis


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ViewType* \[ de\]
</dt> <dd>

**Cadena** que especifica el tipo de elemento que se va a agregar al panel lista. El autor de la llamada debe establecer este parámetro en una de las siguientes [constantes de ubicación de biblioteca](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*Viewid controles* \[ de\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos que se van a agregar al panel lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExternalObject para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





