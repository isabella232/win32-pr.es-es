---
title: Método External.buy
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método de compra inicia la compra de un conjunto de elementos multimedia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- comprar método Reproductor de Windows Media
- método buy Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media , método buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acc578d18c2a93118e1d7aa55b0fdcbe474a8698a0982ef8c2df7edb3802ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649525"
---
# <a name="externalbuy-method"></a>Método External.buy

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método de** compra inicia la compra de un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ViewType* \[ En\]
</dt> <dd>

**Cadena** que especifica el tipo de elemento que se va a comprar. El autor de la llamada debe establecer este parámetro en una de las siguientes constantes [de ubicación de biblioteca:](library-location-constants.md)

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*ViewIDs* \[ En\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los artículos que se comprarán.

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

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner::Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Compra de contenido multimedia**](purchasing-media-content.md)
</dt> </dl>

 

 





