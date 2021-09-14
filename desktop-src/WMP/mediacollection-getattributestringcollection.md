---
title: Método MediaCollection.getAttributeStringCollection
description: El método getAttributeStringCollection recupera un objeto StringCollection que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Método getAttributeStringCollection Reproductor de Windows Media
- Método getAttributeStringCollection Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media , método getAttributeStringCollection
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068383"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Método MediaCollection.getAttributeStringCollection

El **método getAttributeStringCollection** recupera un objeto **StringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que especifica el atributo.

</dd> <dt>

*mediaType* \[ En\]
</dt> <dd>

**Cadena que** representa el tipo de medio. Contiene uno de los valores siguientes: "Audio", "Video", "Playlist" u "Other".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto StringCollection.**

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la sección [Referencia de](attribute-reference.md) atributos.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getAttributeStringCollection para** mostrar una lista de valores que corresponden a un atributo determinado para los elementos de audio de la colección multimedia. Un elemento SELECT HTML, creado con id. = "Atributo", permite al usuario seleccionar un atributo, como Artist, Genre o Album. Un elemento TEXTAREA HTML, creado con id. = "AttributeVals", muestra el resultado. El **objeto Player** se creó con id. = "Player".


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
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





