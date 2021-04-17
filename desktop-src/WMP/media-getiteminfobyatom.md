---
title: Método media. getItemInfoByAtom
description: El método getItemInfoByAtom recupera el valor del atributo con el número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- método getItemInfoByAtom de Windows Media Player
- método getItemInfoByAtom Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700235"
---
# <a name="mediagetiteminfobyatom-method"></a>Método media. getItemInfoByAtom

El método **getItemInfoByAtom** recupera el valor del atributo con el número de índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice en el que un atributo determinado reside en el conjunto de atributos disponibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que representa el valor del atributo especificado. En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Este método se puede utilizar para recuperar los metadatos de un elemento multimedia digital específico mediante un número de índice de atributo. La propiedad **attributeCount** se puede utilizar para determinar el número de atributos disponibles para el elemento multimedia.

El método **getMediaAtom** del objeto **MediaCollection** también se puede usar para recuperar el índice de un atributo determinado. Esta técnica suele ser más eficaz que los métodos **getItemInfo** o **getItemInfoByType** al trabajar con listas de reproducción grandes.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





