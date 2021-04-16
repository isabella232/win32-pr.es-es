---
title: StringCollection. getItemInfo (método)
description: El método getItemInfo recupera la cadena correspondiente al índice y el nombre del elemento StringCollection especificado.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718788"
---
# <a name="stringcollectiongetiteminfo-method"></a>StringCollection. getItemInfo (método)

El método **getItemInfo** recupera la cadena correspondiente al índice y el nombre del elemento **StringCollection** especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que representa el valor del atributo especificado. En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





