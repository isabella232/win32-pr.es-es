---
title: Método Media.getItemInfo
description: El método getItemInfo recupera el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , Clase Media
- Clase media Reproductor de Windows Media , método getItemInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068421"
---
# <a name="mediagetiteminfo-method"></a>Método Media.getItemInfo

El **método getItemInfo** recupera el valor del atributo especificado para el elemento multimedia actual.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto String** que representa el valor del atributo especificado. Para los atributos cuyo valor subyacente **es booleano,** devuelve la cadena "true" o "false".

## <a name="remarks"></a>Observaciones

Este método recupera los metadatos de un elemento multimedia digital individual o un elemento multimedia que forma parte de una lista de reproducción.

La **propiedad attributeCount** contiene el número de nombres de atributo disponibles para un objeto **Multimedia** determinado. Los números de índice se pueden usar con el **método getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar **a getItemInfo.**

Para recuperar atributos con varios valores y atributos con valores complejos, use el **método getItemInfoByType.**

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para compartir las bibliotecas Windows multimedia a través de UPnP, Reproductor de Windows Media crea un servicio de directorio de contenido (CDS) que se expone a través de UPnP. A continuación, otros dispositivos pueden navegar y examinar las bibliotecas.

En Windows 7, una aplicación puede usar los atributos Reproductor de Windows Media [**TrackingID**](trackingid-attribute.md) y [**MediaType**](mediatype-attribute.md) para construir el identificador de objeto de cada elemento del CDS. Tenga en cuenta que esta construcción puede cambiar en versiones futuras de Windows. La aplicación pasa cada una de estas cadenas de atributo en el *parámetro name* en una llamada a **getItemInfo**. **getItemInfo** devuelve el valor de cada atributo del valor devuelto. A continuación, la aplicación usa la siguiente sintaxis para construir cada identificador de objeto:

*TrackingID*.0. *MediaTypeID*

Esta sintaxis tiene el significado siguiente:

-   *TrackingID* es la cadena que se almacena en el Reproductor de Windows Media [**TrackingID**](trackingid-attribute.md) del elemento multimedia.
-   *MediaTypeID* depende del valor del atributo [**MediaType,**](mediatype-attribute.md) como se muestra en la tabla siguiente:

    | Atributo MediaType                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Elementos de audio](audio-item-attributes.md) | 4           |
    | [Elementos de fotos](photo-item-attributes.md) | B           |
    | [Elementos de vídeo](video-item-attributes.md) | 8           |

    

     

**Reproductor de Windows Media 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de elementos multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





