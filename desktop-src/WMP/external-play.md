---
title: Método External.play
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método de reproducción indica Reproductor de Windows Media reproducir un conjunto de elementos multimedia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- método play Reproductor de Windows Media
- play method Reproductor de Windows Media , External (Clase)
- Clase externa Reproductor de Windows Media , método play
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
ms.openlocfilehash: 90644b357e56f40bfbdb576908b99aa6941f8153dc339daa996152f63d77372c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648635"
---
# <a name="externalplay-method"></a>Método External.play

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **método de** reproducción indica Reproductor de Windows Media reproducir un conjunto de elementos multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LibraryLocationType* \[ En\]
</dt> <dd>

Constante [de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de elementos multimedia que se reproducirán. Por ejemplo, CPAlbumID especifica que se van a reproducir uno o varios discos.

</dd> <dt>

*LibraryLocationIDs* \[ En\]
</dt> <dd>

**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se reproducirán.

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
</dt> </dl>

 

 





