---
title: Método MediaCollection.getByAttributeAndMediaType
description: El método getByAttributeAndMediaType recupera un objeto Playlist que contiene objetos Media que tienen el atributo y el tipo de medio especificados.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Método getByAttributeAndMediaType Reproductor de Windows Media
- Método getByAttributeAndMediaType Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getByAttributeAndMediaType
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
ms.openlocfilehash: 46dab1bdcb511e4c96374b17bc6a98be95e48fd64d005eb856c9ec247af48f2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647885"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Método MediaCollection.getByAttributeAndMediaType

El **método getByAttributeAndMediaType** recupera un objeto **Playlist** que contiene objetos **Media** que tienen el atributo y el tipo de medio especificados.

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

*atributo* \[ En\]
</dt> <dd>

**Cadena** que contiene el atributo.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

**Cadena** que contiene el valor.

</dd> <dt>

*mediaType* \[ En\]
</dt> <dd>

**Cadena** que contiene el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 





