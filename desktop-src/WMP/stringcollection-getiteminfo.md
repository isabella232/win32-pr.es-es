---
title: Método StringCollection.getItemInfo
description: El método getItemInfo recupera la cadena correspondiente al índice y el nombre del elemento StringCollection especificados.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , clase StringCollection
- Clase StringCollection Reproductor de Windows Media método , getItemInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570085"
---
# <a name="stringcollectiongetiteminfo-method"></a>Método StringCollection.getItemInfo

El **método getItemInfo** recupera la cadena correspondiente al índice y el nombre del **elemento StringCollection** especificados.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto String** que representa el valor del atributo especificado. Para los atributos cuyo valor subyacente **es booleano,** devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Para recuperar atributos con varios valores y atributos con valores complejos, use el **método getItemInfoByType.**

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**StringCollection.getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





