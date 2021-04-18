---
title: Método media. isReadOnlyItem
description: El método isReadOnlyItem devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- método isReadOnlyItem de Windows Media Player
- método isReadOnlyItem Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698470"
---
# <a name="mediaisreadonlyitem-method"></a>Método media. isReadOnlyItem

El método **isReadOnlyItem** devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que indica el nombre del atributo que se va a probar. Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Si un atributo es de solo lectura, no se puede establecer con el método **setItemInfo** . Tenga en cuenta que este método puede devolver valores diferentes para un atributo determinado cuando se usa con versiones diferentes de Windows Media Player.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **true**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **isReadOnlyItem** para rellenar un elemento TEXTAREA HTML denominado rwText con información sobre el elemento multimedia actual. El código genera cada atributo del elemento multimedia actual, junto con el texto que indica si el atributo es de solo lectura o de lectura y escritura. El objeto **Player** se creó con ID = "Player".


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





