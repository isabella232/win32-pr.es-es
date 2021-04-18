---
title: Elemento PARAM (WMP SDK)
description: El elemento PARAM define un parámetro personalizado asociado a una lista de reproducción o un elemento de una lista de reproducción.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Elemento PARAM de Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700233"
---
# <a name="param-element"></a>Elemento PARAM

El elemento **param** define un parámetro personalizado asociado a una lista de reproducción o un elemento de una lista de reproducción.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Parámetros

Un parámetro también se puede asociar a la presentación en lugar de a un clip individual, colocando este elemento directamente después de la etiqueta **ASX** . Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.

> [!Note]  
> Este elemento **ASX** solo está disponible para Windows Media Player versión 6,01 y versiones posteriores. La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Windows Media Player.

 

## <a name="attributes"></a>Atributos

**NOMBRE**

Nombre usado para obtener acceso al valor del parámetro. El nombre puede ser cualquier cadena válida. Ya se han definido las siguientes cadenas.



| String                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | El atributo **valor** especifica si la lista de reproducción del metarchivo permite a Windows Media Player característica de orden aleatorio para reproducir las entradas en orden aleatorio. El atributo de **valor** se puede establecer en "sí" o "no". El valor predeterminado es "no".                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | El atributo **Value** especifica si el usuario puede pausar la reproducción. El atributo de **valor** se puede establecer en "sí" o "no". El valor predeterminado es "Yes".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | El atributo **valor** especifica si el usuario puede cambiar la posición de reproducción actual mediante la barra de búsqueda, el avance rápido o el retroceso rápido. El atributo de **valor** se puede establecer en "sí" o "no". El valor predeterminado es "Yes".                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | El atributo **valor** especifica si el usuario puede omitir el elemento anterior de la lista de reproducción haciendo clic en **anterior**. El atributo de **valor** se puede establecer en "sí" o "no". El valor predeterminado es "Yes".                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | El atributo **valor** especifica si el usuario puede saltar hacia delante hasta el siguiente elemento de la lista de reproducción haciendo clic en **siguiente**. El atributo de **valor** se puede establecer en "sí" o "no". El valor predeterminado es "Yes".                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | El atributo **Value** especifica el identificador de una fuente de radio proporcionada por un almacén en línea de tipo 1. Es decir, el atributo de **valor** debe ser igual que el campo RadioID de una de las fuentes de radio del catálogo de la tienda en línea. El elemento primario es el elemento **ASX** .                                                                                                                                                                                                                                                                                                                                   |
| Encoding                        | El atributo de **valor** se establece en "UTF-8" para indicar que el metarchivo es un archivo codificado de Unicode (UTF-8).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | El atributo **Value** es una cadena que proporciona un almacén en línea de tipo 1. Windows Media Player pasa la cadena al método [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , que se implementa mediante el complemento de la tienda en línea. El método **GetItemInfo** devuelve la dirección URL de la página web que se va a mostrar en el panel **reproducción en curso** del reproductor. La página web tiene acceso a todos los métodos que expone el objeto **externo** a los almacenes de tipo 1. Para obtener una lista de estos métodos, consulte [objeto externo para las tiendas en línea de tipo 1](external-object-for-type-1-online-stores.md). |
| HTMLView                        | El atributo **valor** especifica una dirección URL que se muestra en el panel **reproducción en curso** del reproductor en modo completo mientras dure la lista de reproducción o la entrada actual, dependiendo de si el elemento primario es el elemento **ASX** o un elemento de **entrada** . HTMLView no es compatible con el control de Media Player de Windows.                                                                                                                                                                                                                                                                               |
| Log:*FieldName* \[ :*namespace*\] | El atributo **Value** especifica el valor en el que se establecerá el campo de registro indicado. La parte del *espacio de nombres* : del atributo **Name** es opcional.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Búfer                       | El atributo **valor** especifica si la siguiente entrada de lista de reproducción comienza el almacenamiento en búfer antes del final de la entrada actual, lo que permite una transición sin problemas. El atributo de **valor** se puede establecer en "true" o "false".                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | El atributo **Value** especifica si un archivo de imagen al que hace referencia el elemento de **entrada** actual continúa mostrándose más allá de su tiempo de duración especificado mientras se almacena en búfer la siguiente entrada de lista de reproducción. El atributo de **valor** se puede establecer en "true" o "false".                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Valor asociado a este parámetro. Puede ser un valor numérico o de cadena.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento permite a los usuarios colocar información adicional sobre cada clip dentro del elemento de **entrada** que lo contiene. Para recuperar la información de metadatos especificada en la **entrada** de la lista de reproducción, utilice el *medio*. método **getItemInfo** . El *medio*. el método **getItemInfo** recupera el valor del atributo **Value** , dado el nombre del parámetro. Las versiones anteriores de Windows Media Player recuperar la información de metadatos especificada en la **entrada** de la lista de reproducción, mediante el método **GetMediaParameter** dado el nombre del parámetro y un número de índice de la entrada.

Un parámetro también se puede asociar a la presentación en lugar de a un clip individual, colocando este elemento directamente después de la etiqueta **ASX** . Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.

**Note**

Este elemento **ASX** solo está disponible para Windows Media Player versión 6,01 y versiones posteriores. La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Windows Media Player.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior, se requiere Windows Media Player 9 series o posterior para los atributos de nombre predefinidos, se requiere Windows Media Player 10 o posterior para los nombres predefinidos CanPause, CanSeek, CanSkipBack y CanSkipForward<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Datos de la secuencia de registro**](logging-stream-data.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





