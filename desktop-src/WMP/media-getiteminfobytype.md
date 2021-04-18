---
title: Método media. getItemInfoByType
description: El método getItemInfoByType recupera el valor del atributo correspondiente al nombre de atributo, el idioma y el índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700234"
---
# <a name="mediagetiteminfobytype-method"></a>Método media. getItemInfoByType

El método **getItemInfoByType** recupera el valor del atributo correspondiente al nombre de atributo, el idioma y el índice especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> <dt>

*idioma* \[ de de\]
</dt> <dd>

**Cadena** que representa el idioma. Si el valor se establece en null o en "" (cadena vacía), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice de base cero del valor que se va a recuperar del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número**, una **cadena**, un objeto **MetadataPicture** o un objeto **MetadataText** , como se indica en la tabla siguiente.



| Atributo                   | Valor devuelto                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Número** (**unsigned Long**) |
| **WM/Letras \_ sincronizadas** | Objeto **MetadataText**        |
| **WM/imagen**              | Objeto **MetadataPicture**     |
| **WM/UserWebURL**           | Objeto **MetadataText**        |
| Resto de atributos        | **String**                     |



 

En el caso de los atributos cuyo valor subyacente es **booleano**, este método devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Este método recupera los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.

Este método admite atributos con varios valores y atributos con valores complejos. El método **getItemInfo** no admite atributos con varios valores y atributos con valores complejos.

La propiedad **attributeCount** contiene el número de nombres de atributo disponibles para un objeto **multimedia** determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar al parámetro *Name* de **getItemInfoByType**.

El método **getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un objeto **multimedia** determinado. Los números de índice se pueden pasar al parámetro de *Índice* de **getItemInfoByType**. Esto resulta útil cuando un elemento multimedia digital se ha clasificado en varios géneros, por ejemplo.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Este método puede producir errores. Debe incluir el código de control de errores al llamar a este método. Por ejemplo, en JScript puede implementar el control de errores mediante el uso de la **instrucción try... detectar... Finally** (estructura).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Objeto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objeto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





