---
title: MediaCollection. getAttributeStringCollection, método
description: El método getAttributeStringCollection recupera un objeto StringCollection que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- método getAttributeStringCollection de Windows Media Player
- método getAttributeStringCollection de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690638"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>MediaCollection. getAttributeStringCollection, método

El método **getAttributeStringCollection** recupera un objeto **StringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el atributo.

</dd> <dt>

*mediaType* \[ de\]
</dt> <dd>

**Cadena** que representa el tipo de medio. Contiene uno de los siguientes valores: "audio", "vídeo", "lista de reproducción" u "otro".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **StringCollection** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos que admite Windows Media Player, consulte la sección [referencia de atributos](attribute-reference.md) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **getAttributeStringCollection** para mostrar una lista de valores que corresponden a un atributo determinado para los elementos de audio de la colección de medios. Un elemento SELECT de HTML, creado con ID = "Attribute", permite al usuario seleccionar un atributo, como artista, género o álbum. Un elemento TEXTAREA HTML, creado con ID = "AttributeVals", muestra el resultado. El objeto **Player** se creó con ID = "Player".


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





