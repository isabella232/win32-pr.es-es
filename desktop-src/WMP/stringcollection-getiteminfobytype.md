---
title: StringCollection. getItemInfoByType (método)
description: El método getItemInfoByType recupera el valor correspondiente al índice de la StringCollection, el nombre, el idioma y el índice de atributo especificados.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getItemInfoByType
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
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718705"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. getItemInfoByType (método)

El método **getItemInfoByType** recupera el valor correspondiente al índice de la **StringCollection** , el nombre, el idioma y el índice de atributo especificados.

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

*Índice* \[ de de\]
</dt> <dd>

**Número** (**Long**) que especifica el índice de base cero del elemento **StringCollection** del que se va a obtener el atributo.

</dd> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*idioma* \[ de de\]
</dt> <dd>

**Cadena** que contiene el idioma. Si el valor se establece en null o en una cadena vacía (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".

</dd> <dt>

*attributeIndex* \[ de\]
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
| Resto de atributos        | String                         |



 

En el caso de los atributos cuyo valor subyacente es **booleano**, este método devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Este método admite atributos con varios valores y atributos con valores complejos. El método **getItemInfo** no admite atributos con valores múltiples o complejos.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objeto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





