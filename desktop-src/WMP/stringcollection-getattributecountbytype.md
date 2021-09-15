---
title: Método StringCollection.getAttributeCountByType
description: El método getAttributeCountByType recupera el número de atributos asociados al índice del elemento StringCollection, el nombre de atributo y el idioma especificados.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Método getAttributeCountByType Reproductor de Windows Media
- Método getAttributeCountByType Reproductor de Windows Media , clase StringCollection
- Clase StringCollection Reproductor de Windows Media método , getAttributeCountByType
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570089"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>Método StringCollection.getAttributeCountByType

El **método getAttributeCountByType** recupera el número de atributos asociados al índice del elemento **StringCollection,** el nombre de atributo y el idioma especificados.

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

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice de base cero del **elemento StringCollection** del que se va a obtener el atributo.

</dd> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*idioma* \[ En\]
</dt> <dd>

**Cadena** que contiene el idioma. Si el valor se establece en null o en la cadena vacía (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de lenguaje RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Observaciones

Este método se usa para determinar el número de atributos correspondientes a un nombre de atributo determinado para un elemento **StringCollection** determinado. A continuación, los números de índice se pueden pasar al cuarto parámetro del **método StringCollection.getItemInfoByType.**

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**StringCollection (objeto)**](stringcollection-object.md)
</dt> </dl>

 

 





