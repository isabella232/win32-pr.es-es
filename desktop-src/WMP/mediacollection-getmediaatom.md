---
title: Método MediaCollection.getMediaAtom
description: El método getMediaAtom recupera el índice en el que reside un atributo especificado dentro del conjunto de atributos disponibles.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Método getMediaAtom Reproductor de Windows Media
- Método getMediaAtom Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getMediaAtom
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
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837208"
---
# <a name="mediacollectiongetmediaatom-method"></a>Método MediaCollection.getMediaAtom

El **método getMediaAtom** recupera el índice en el que reside un atributo especificado dentro del conjunto de atributos disponibles.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Comentarios

El número de índice recuperado con este método se puede pasar *al* medio . **Método getItemInfoByAtom** para tener acceso a los valores de atributo. Esta técnica suele ser más eficaz cuando se trabaja con listas de reproducción grandes que al acceder a un valor de atributo por nombre a través de *Media*. **getItemInfo o** *Media*. **getItemInfoByType**.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





