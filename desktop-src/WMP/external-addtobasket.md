---
title: Método External.addToBasket
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Método External.addToBasket
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Método addToBasket Reproductor de Windows Media
- Método addToBasket Reproductor de Windows Media , clase External
- Clase externa Reproductor de Windows Media , método addToBasket
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
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650015"
---
# <a name="externaladdtobasket-method"></a>Método External.addToBasket

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método addToBasket** agrega elementos multimedia al panel de lista (también denominado cesta) en Reproductor de Windows Media.

## <a name="syntax"></a>Sintaxis


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ViewType* \[ En\]
</dt> <dd>

**Cadena** que especifica el tipo de elemento que se va a agregar al panel de lista. El autor de la llamada debe establecer este parámetro en una de las siguientes constantes [de ubicación de biblioteca:](library-location-constants.md)

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*ViewIDs* \[ En\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos que se van a agregar al panel de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExternalObject para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





