---
title: Método media. getAttributeCountByType
description: El método getAttributeCountByType recupera el número de atributos asociados al nombre de atributo y el idioma especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700237"
---
# <a name="mediagetattributecountbytype-method"></a>Método media. getAttributeCountByType

El método **getAttributeCountByType** recupera el número de atributos asociados al nombre de atributo y el idioma especificados.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**) que contiene el número de atributos.

## <a name="remarks"></a>Observaciones

Este método se utiliza para determinar el número de atributos correspondientes a un nombre de atributo determinado para un objeto **multimedia** determinado. Después, los números de índice se pueden pasar al método **getItemInfoByType** . Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





