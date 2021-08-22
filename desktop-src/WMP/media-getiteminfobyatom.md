---
title: Método Media.getItemInfoByAtom
description: El método getItemInfoByAtom recupera el valor del atributo con el número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Método getItemInfoByAtom Reproductor de Windows Media
- Método getItemInfoByAtom Reproductor de Windows Media , clase Media
- Clase multimedia Reproductor de Windows Media método , getItemInfoByAtom
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
ms.openlocfilehash: 26db8e87a52c0d8c8236b5e4b8b5e7325fb3bb0a995dcbd81da668ea760df660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135138"
---
# <a name="mediagetiteminfobyatom-method"></a>Método Media.getItemInfoByAtom

El **método getItemInfoByAtom** recupera el valor del atributo con el número de índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice en el que reside un atributo determinado dentro del conjunto de atributos disponibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto String** que representa el valor del atributo especificado. Para los atributos cuyo valor subyacente **es booleano,** devuelve la cadena "true" o "false".

## <a name="remarks"></a>Comentarios

Este método se puede usar para recuperar los metadatos de un elemento multimedia digital específico mediante un número de índice de atributo. La **propiedad attributeCount** se puede usar para determinar el número de atributos disponibles para el elemento multimedia.

El **método getMediaAtom** del **objeto MediaCollection** también se puede usar para recuperar el índice de un atributo determinado. Esta técnica suele ser más eficaz que los **métodos getItemInfo** o **getItemInfoByType** al trabajar con listas de reproducción grandes.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

**Reproductor de Windows Media 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lectura de valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





