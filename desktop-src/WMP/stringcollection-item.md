---
title: StringCollection. Item (método)
description: El método Item recupera la cadena en el índice especificado.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718625"
---
# <a name="stringcollectionitem-method"></a>StringCollection. Item (método)

El método **Item** recupera la cadena en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

El objeto **StringCollection** se utiliza para recuperar el conjunto de valores disponibles para un atributo. Por ejemplo, *MediaCollection*. el método **getAttributeStringCollection** se puede utilizar para recuperar un objeto **StringCollection** que representa todos los valores del atributo Genre en el tipo de medios de audio. La propiedad **Item** se puede usar para recorrer en iteración todos los valores posibles del atributo Genre.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection.getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





