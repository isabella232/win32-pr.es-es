---
title: Método MediaCollection.getAttributeStringCollection
description: El método getAttributeStringCollection recupera un objeto StringCollection que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Método getAttributeStringCollection Reproductor de Windows Media
- Método getAttributeStringCollection Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getAttributeStringCollection
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
ms.openlocfilehash: c27b7c6dbef585763ecfda1abdc7beadfa3d883476033424ff868a3d56c4bb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996314"
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

**Cadena que** representa el tipo de medio. Contiene uno de los siguientes valores: "Audio", "Vídeo", "Lista de reproducción" u "Otro".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto StringCollection.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la sección [Referencia de](attribute-reference.md) atributos.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getAttributeStringCollection** para mostrar una lista de valores que corresponden a un atributo determinado para los elementos de audio de la colección multimedia. Un elemento SELECT HTML, creado con id. = "Atributo", permite al usuario seleccionar un atributo, como Artist, Genre o Album. Un elemento TEXTAREA HTML, creado con id. = "AttributeVals", muestra el resultado. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





