---
title: MediaCollection. getByAttributeAndMediaType, método
description: El método getByAttributeAndMediaType recupera un objeto de lista de reproducción que contiene objetos multimedia que tienen el atributo y el tipo de medio especificados.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- método getByAttributeAndMediaType de Windows Media Player
- método getByAttributeAndMediaType de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649957"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>MediaCollection. getByAttributeAndMediaType, método

El método **getByAttributeAndMediaType** recupera un objeto de **lista de reproducción** que contiene objetos **multimedia** que tienen el atributo y el tipo de medio especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que contiene el atributo.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

**Cadena** que contiene el valor.

</dd> <dt>

*mediaType* \[ de\]
</dt> <dd>

**Cadena** que contiene el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> </dl>

 

 





