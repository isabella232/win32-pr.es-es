---
title: Método Media.setItemInfo
description: El método setItemInfo establece el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Método setItemInfo Reproductor de Windows Media
- Método setItemInfo Reproductor de Windows Media , Clase Media
- Clase multimedia Reproductor de Windows Media método , setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068389"
---
# <a name="mediasetiteminfo-method"></a>Método Media.setItemInfo

El **método setItemInfo** establece el valor del atributo especificado para el elemento multimedia actual.

## <a name="syntax"></a>Sintaxis


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*value* \[ En\]
</dt> <dd>

**Cadena** que contiene el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **propiedad attributeCount** contiene el número de atributos disponibles para un objeto **Media** determinado. Los números de índice se pueden usar con el **método getAttributeName** para determinar los nombres de los atributos integrados que se pueden usar con este método.

Antes de usar este método, use el **método isReadOnlyItem** para determinar si se puede establecer un atributo determinado.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

**Note**

Si inserta el control Reproductor de Windows Media en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Reproductor de Windows Media. Si usa el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están disponibles inmediatamente para el código a través de la biblioteca.

**Reproductor de Windows Media 10 Mobile:** Este método no se implementa.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **setItemInfo** para cambiar el valor del atributo Genre del elemento multimedia actual. Un elemento de entrada HTML TEXT denominado genText permite al usuario escribir una cadena de texto, que luego se usa para cambiar la información del atributo. El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





