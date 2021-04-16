---
title: StringCollection. getAttributeCountByType (método)
description: El método getAttributeCountByType recupera el número de atributos asociados con el índice del elemento StringCollection, el nombre de atributo y el idioma especificados.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718783"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. getAttributeCountByType (método)

El método **getAttributeCountByType** recupera el número de atributos asociados con el índice del elemento **StringCollection** , el nombre de atributo y el idioma especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Este método se utiliza para determinar el número de atributos correspondientes a un nombre de atributo determinado para un elemento **StringCollection** determinado. Los números de índice se pueden pasar al cuarto parámetro del método **StringCollection. getItemInfoByType** .

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





