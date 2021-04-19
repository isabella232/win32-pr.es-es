---
title: Método media. setItemInfo
description: El método setItemInfo establece el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método setItemInfo
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699955"
---
# <a name="mediasetiteminfo-method"></a>Método media. setItemInfo

El método **setItemInfo** establece el valor del atributo especificado para el elemento multimedia actual.

## <a name="syntax"></a>Sintaxis


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nuevo valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La propiedad **attributeCount** contiene el número de atributos disponibles para un objeto **multimedia** determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar los nombres de los atributos integrados que se pueden usar con este método.

Antes de utilizar este método, utilice el método **isReadOnlyItem** para determinar si se puede establecer un atributo determinado.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Note**

Si incrusta el control Media Player de Windows en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Media Player de Windows. Si utiliza el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios. En cualquier caso, los cambios están inmediatamente disponibles para el código a través de la biblioteca.

**Windows Media Player 10 Mobile:** Este método no está implementado.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **setItemInfo** para cambiar el valor del atributo Genre del elemento multimedia actual. Un elemento de entrada de texto HTML denominado genText permite al usuario escribir una cadena de texto, que se usa para cambiar la información de atributo. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





