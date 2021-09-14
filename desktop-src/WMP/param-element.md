---
title: Elemento PARAM (SDK de WMP)
description: El elemento PARAM define un parámetro personalizado asociado a una lista de reproducción o a un elemento de una lista de reproducción.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Elemento PARAM Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967311"
---
# <a name="param-element"></a>Elemento PARAM

El **elemento PARAM** define un parámetro personalizado asociado a una lista de reproducción o a un elemento de una lista de reproducción.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Parámetros

Un parámetro también se puede asociar a la presentación en lugar de a un clip individual colocando este elemento directamente después de la **etiqueta ASX.** Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.

> [!Note]  
> Este **elemento ASX** solo está disponible para Reproductor de Windows Media versión 6.01 y posteriores. La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Reproductor de Windows Media.

 

## <a name="attributes"></a>Atributos

**NOMBRE**

Nombre utilizado para tener acceso al valor del parámetro. El nombre puede ser cualquier cadena válida. Ya se han definido las cadenas siguientes.



| String                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | El **atributo VALUE** especifica si la lista de reproducción de metarchivo permite que Reproductor de Windows Media de orden aleatorio reprodúzca las entradas en orden aleatorio. El **atributo VALUE** se puede establecer en "Yes" o "No". El valor predeterminado es "No".                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | El **atributo VALUE** especifica si el usuario puede pausar la reproducción. El **atributo VALUE** se puede establecer en "Yes" o "No". El valor predeterminado es "Sí".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | El **atributo VALUE** especifica si el usuario puede cambiar la posición de reproducción actual mediante la barra de búsqueda, avance rápido o retroceso rápido. El **atributo VALUE** se puede establecer en "Yes" o "No". El valor predeterminado es "Sí".                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | El **atributo VALUE** especifica si el usuario puede ir al elemento de lista de reproducción anterior haciendo clic en **Anterior.** El **atributo VALUE** se puede establecer en "Yes" o "No". El valor predeterminado es "Sí".                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | El **atributo VALUE** especifica si el usuario puede ir directamente al siguiente elemento de lista de reproducción haciendo clic en **Siguiente.** El **atributo VALUE** se puede establecer en "Yes" o "No". El valor predeterminado es "Sí".                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | El **atributo VALUE** especifica el identificador de una fuente de radio proporcionada por un almacén en línea de tipo 1. Es decir, el **atributo VALUE** debe ser igual al campo RadioID de una de las fuentes de radio del catálogo de la tienda en línea. El elemento primario es el **elemento ASX.**                                                                                                                                                                                                                                                                                                                                   |
| Encoding                        | El **atributo VALUE** se establece en "utf-8" para indicar que el metarchivo es un archivo codificado Unicode (UTF-8).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | El **atributo VALUE** es una cadena proporcionada por un almacén en línea de tipo 1. Reproductor de Windows Media pasa la cadena al método [IWMPContentPartner::GetItemInfo,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) que se implementa mediante el complemento de la tienda en línea. El **método GetItemInfo** devuelve la dirección URL de la página web que se mostrará en el panel **Reproducción** ahora del reproductor. La página web tiene acceso a todos los métodos que el **objeto External** expone a los almacenes de tipo 1. Para obtener una lista de esos métodos, vea [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md). |
| HTMLView                        | El **atributo VALUE** especifica una dirección  URL que se muestra en el panel Reproducción ahora del reproductor en modo completo mientras dure la lista de reproducción o la entrada actual, dependiendo de si el elemento primario es el elemento **ASX** o un **elemento ENTRY.** HTMLView no se admite para el control Reproductor de Windows Media.                                                                                                                                                                                                                                                                               |
| Log:*FieldName* \[ :*NameSpace*\] | El **atributo VALUE** especifica el valor en el que se establecerá el campo de registro indicado. La parte :*NameSpace* del **atributo NAME** es opcional.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Búfer previo                       | El **atributo VALUE** especifica si la siguiente entrada de lista de reproducción comienza a almacenarse en búfer antes del final de la entrada actual, lo que permite una transición sin problemas. El **atributo VALUE** se puede establecer en "true" o "false".                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | El **atributo VALUE** especifica si un archivo de imagen al que hace referencia el elemento **ENTRY** actual sigue a la vista más allá del tiempo de duración especificado mientras se almacena en búfer la siguiente entrada de la lista de reproducción. El **atributo VALUE** se puede establecer en "true" o "false".                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Valor asociado a este parámetro. Puede ser un valor numérico o de cadena.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento permite a los usuarios colocar información adicional sobre cada clip dentro del **elemento ENTRY** que lo contiene. Para recuperar la información de metadatos especificada en la **lista de reproducción ENTRY**, use media .  **Método getItemInfo.** El *medio*. **El método getItemInfo** recupera el valor del **atributo VALUE,** dado el nombre del parámetro. Las versiones anteriores de Reproductor de Windows Media información de metadatos especificada en la lista de reproducción **ENTRY**, mediante el método **GetMediaParameter** dado el nombre del parámetro y un número de índice para la entrada.

Un parámetro también se puede asociar a la presentación en lugar de a un clip individual colocando este elemento directamente después de la **etiqueta ASX.** Se hace referencia a estos elementos por sus nombres y un valor de índice que empieza por cero.

**Nota**

Este **elemento ASX** solo está disponible para Reproductor de Windows Media versión 6.01 y posteriores. La instalación estándar de Microsoft Internet Explorer 5 incluye una versión compatible de Reproductor de Windows Media.

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior, se requiere Reproductor de Windows Media serie 9 o posterior para los atributos NAME predefinidos, se requiere Reproductor de Windows Media 10 o posterior para los nombres predefinidos CanPause, CanSeek, CanSkipBack y CanSkipForward.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Registro de datos de flujo**](logging-stream-data.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





