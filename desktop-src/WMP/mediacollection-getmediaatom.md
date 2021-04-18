---
title: MediaCollection. getMediaAtom, método
description: El método getMediaAtom recupera el índice en el que un atributo especificado reside en el conjunto de atributos disponibles.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- método getMediaAtom de Windows Media Player
- método getMediaAtom de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690358"
---
# <a name="mediacollectiongetmediaatom-method"></a>MediaCollection. getMediaAtom, método

El método **getMediaAtom** recupera el índice en el que un atributo especificado reside en el conjunto de atributos disponibles.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

El número de índice recuperado con este método se puede pasar a los *medios*. método **getItemInfoByAtom** para tener acceso a los valores de atributo. Esta técnica suele ser más eficaz al trabajar con listas de reproducción de gran tamaño que el acceso a un valor de atributo por nombre a través de *medios*. **getItemInfo** o *multimedia*. **getItemInfoByType**.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





