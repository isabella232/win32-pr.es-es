---
title: Método Media.getItemInfoByType
description: El método getItemInfoByType recupera el valor del atributo correspondiente al nombre de atributo, idioma e índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- Método getItemInfoByType Reproductor de Windows Media
- Método getItemInfoByType Reproductor de Windows Media , clase Media
- Clase multimedia Reproductor de Windows Media método , getItemInfoByType
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
ms.openlocfilehash: aa180834d70c8dd078beafc360400c931e7058994f1cc46d4e9abb011987d158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135128"
---
# <a name="mediagetiteminfobytype-method"></a>Método Media.getItemInfoByType

El **método getItemInfoByType** recupera el valor del atributo correspondiente al nombre de atributo, idioma e índice especificados.

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

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*idioma* \[ En\]
</dt> <dd>

**Cadena** que representa el idioma. Si el valor se establece en null o "" (cadena vacía), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-us".

</dd> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice de base cero del valor que se recuperará del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto Number**, **String**, **MetadataPicture** u **MetadataText,** como se indica en la tabla siguiente.



| Atributo                   | Valor devuelto                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **\_WM/Synchronised** | **Objeto MetadataText**        |
| **WM/Picture**              | **Objeto MetadataPicture**     |
| **WM/UserWebURL**           | **Objeto MetadataText**        |
| Resto de atributos        | **String**                     |



 

Para los atributos cuyo valor subyacente es **booleano,** este método devuelve la cadena "true" o "false".

## <a name="remarks"></a>Comentarios

Este método recupera los metadatos de un elemento multimedia digital individual o un elemento multimedia que forma parte de una lista de reproducción.

Este método admite atributos con varios valores y atributos con valores complejos. El **método getItemInfo** no admite atributos con varios valores y atributos con valores complejos.

La **propiedad attributeCount** contiene el número de nombres de atributo disponibles para un objeto **Multimedia** determinado. Los números de índice se pueden usar con el **método getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar al *parámetro name* **de getItemInfoByType**.

El **método getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un objeto **Media** determinado. A continuación, se pueden pasar números de índice al *parámetro index* **de getItemInfoByType**. Esto resulta útil cuando un elemento multimedia digital se ha clasificado en varios géneros, por ejemplo.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Este método puede producir errores. Debe incluir código de control de errores al llamar a este método. Por ejemplo, en JScript puede implementar el control de errores mediante **el método try... atrapar... finally** (Estructura).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MetadataPicture (objeto)**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText (objeto)**](metadatatext-object.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





