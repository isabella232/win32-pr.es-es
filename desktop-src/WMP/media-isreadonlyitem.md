---
title: Método Media.isReadOnlyItem
description: El método isReadOnlyItem devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Método isReadOnlyItem Reproductor de Windows Media
- Método isReadOnlyItem Reproductor de Windows Media , Clase Media
- Clase multimedia Reproductor de Windows Media método , isReadOnlyItem
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
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123395"
---
# <a name="mediaisreadonlyitem-method"></a>Método Media.isReadOnlyItem

El **método isReadOnlyItem** devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que indica el nombre del atributo que se debe probar. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Comentarios

Si un atributo es de solo lectura, no se puede establecer con el **método setItemInfo.** Tenga en cuenta que este método puede devolver valores diferentes para un atributo determinado cuando se usa con versiones diferentes de Reproductor de Windows Media.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve **true.**

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **isReadOnlyItem para** rellenar un elemento TEXTAREA HTML denominado rwText con información sobre el elemento multimedia actual. El código genera cada atributo del elemento multimedia actual, junto con texto que indica si el atributo es de solo lectura o de lectura y escritura. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





