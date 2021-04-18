---
title: External. Play (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método play indica a Windows Media Player que reproduzca un conjunto de elementos multimedia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- método play Windows Media Player
- método play Windows Media Player, clase externa
- Clase externa Windows Media Player, método play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698581"
---
# <a name="externalplay-method"></a>External. Play (método)

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **Play** indica a Windows Media Player que reproduzca un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LibraryLocationType* \[ de\]
</dt> <dd>

Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de los elementos multimedia que se van a reproducir. Por ejemplo, CPAlbumID especifica que se reproducirán uno o más álbumes.

</dd> <dt>

*LibraryLocationIDs* \[ de\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se van a reproducir.

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
</dt> </dl>

 

 





