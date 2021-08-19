---
title: Método StringCollection.getItemInfoByType
description: El método getItemInfoByType recupera el valor correspondiente al índice, el nombre, el idioma y el índice de atributos de StringCollection especificados.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Método getItemInfoByType Reproductor de Windows Media
- Método getItemInfoByType Reproductor de Windows Media , clase StringCollection
- Clase StringCollection Reproductor de Windows Media , método getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9d270ab746618f81f7c2e4135f7a6057f207d2cc89961ebe7c8f47d9fd1abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123035"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>Método StringCollection.getItemInfoByType

El **método getItemInfoByType** recupera el valor correspondiente al índice, el nombre, el idioma y el índice de atributos **de StringCollection** especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice de base cero del **elemento StringCollection** del que se va a obtener el atributo.

</dd> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*idioma* \[ En\]
</dt> <dd>

**Cadena** que contiene el idioma. Si el valor se establece en null o la cadena vacía ("") se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-us".

</dd> <dt>

*attributeIndex* \[ En\]
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
| Resto de atributos        | String                         |



 

Para los atributos cuyo valor subyacente es **booleano,** este método devuelve la cadena "true" o "false".

## <a name="remarks"></a>Comentarios

Este método admite atributos con varios valores y atributos con valores complejos. El **método getItemInfo** no admite atributos con varios valores o complejos.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MetadataPicture (objeto)**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText (objeto)**](metadatatext-object.md)
</dt> <dt>

[**StringCollection.getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





