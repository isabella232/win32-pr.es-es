---
title: Método media. getItemInfo
description: El método getItemInfo recupera el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700236"
---
# <a name="mediagetiteminfo-method"></a>Método media. getItemInfo

El método **getItemInfo** recupera el valor del atributo especificado para el elemento multimedia actual.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que representa el valor del atributo especificado. En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Este método recupera los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.

La propiedad **attributeCount** contiene el número de nombres de atributo disponibles para un objeto **multimedia** determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar a **getItemInfo**.

Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para compartir las bibliotecas de Windows Media a través de UPnP, Windows Media Player crea un servicio de directorio de contenido (CDS) que se expone a través de UPnP. Otros dispositivos pueden navegar y examinar las bibliotecas.

En Windows 7, una aplicación puede usar los atributos [**TrackingID**](trackingid-attribute.md) y [**MediaType**](mediatype-attribute.md) de Windows Media Player para construir el identificador de objeto de cada elemento de los CD. Tenga en cuenta que esta construcción podría cambiar en versiones futuras de Windows. La aplicación pasa cada una de estas cadenas de atributo en el parámetro *Name* en una llamada a **getItemInfo**. **getItemInfo** devuelve el valor de cada atributo en el valor devuelto. A continuación, la aplicación usa la siguiente sintaxis para construir cada identificador de objeto:

*TrackingID*. 0. *MediaTypeID*

Esta sintaxis tiene el significado siguiente:

-   *TrackingID* es la cadena que se almacena en el atributo Windows Media Player [**TrackingID**](trackingid-attribute.md) del elemento multimedia.
-   *MediaTypeID* depende del valor del atributo [**mediatype**](mediatype-attribute.md) , tal como se muestra en la tabla siguiente:

    | MediaType (atributo)                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Elementos de audio](audio-item-attributes.md) | 4           |
    | [Elementos de fotografía](photo-item-attributes.md) | B           |
    | [Elementos de vídeo](video-item-attributes.md) | 8           |

    

     

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

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





