---
title: External. Buy (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método Buy inicia la compra de un conjunto de elementos multimedia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- comprar método Media Player Windows
- método Buy Windows Media Player, clase externa
- Clase externa Windows Media Player, método Buy
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
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699763"
---
# <a name="externalbuy-method"></a>External. Buy (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **Buy** inicia la compra de un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ViewType* \[ de\]
</dt> <dd>

**Cadena** que especifica el tipo de elemento que se va a adquirir. El autor de la llamada debe establecer este parámetro en una de las siguientes [constantes de ubicación de biblioteca](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*Viewid controles* \[ de\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos que se van a adquirir.

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

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner:: Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Compra de contenido multimedia**](purchasing-media-content.md)
</dt> </dl>

 

 





