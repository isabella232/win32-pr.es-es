---
title: Método StringCollection.item
description: El método item recupera la cadena en el índice especificado.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- método item Reproductor de Windows Media
- método item Reproductor de Windows Media , clase StringCollection
- Clase StringCollection Reproductor de Windows Media método , item
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570080"
---
# <a name="stringcollectionitem-method"></a>Método StringCollection.item

El **método** item recupera la cadena en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

El **objeto StringCollection** se usa para recuperar el conjunto de valores disponibles para un atributo. Por ejemplo, *MediaCollection*. **El método getAttributeStringCollection** se puede usar para recuperar un **objeto StringCollection** que representa todos los valores del atributo Genre dentro del tipo de medio Audio. A **continuación,** la propiedad item se puede usar para recorrer en iteración todos los valores posibles para el atributo Genre.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection.getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





