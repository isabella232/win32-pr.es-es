---
title: Elemento REF
description: El elemento REF especifica una dirección URL para el contenido multimedia digital.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF de Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708795"
---
# <a name="ref-element"></a>Elemento REF

El elemento **ref** especifica una dirección URL para el contenido multimedia digital.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL a cualquier parte del contenido multimedia compatible con Windows Media Player.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Elementos primarios | **MOVIMIENTOS**                                                                        |
| Elementos secundarios  | **Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME** |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica una dirección URL para un fragmento de contenido multimedia. La dirección URL puede apuntar a cualquier tipo de medio admitido, mediante cualquier protocolo compatible con Windows Media Player.

Entre los tipos de medios admitidos se incluyen imágenes fijas como imágenes. gif y. jpg y archivos Flash con una extensión de nombre de archivo. SWF. Estos tipos de medios son útiles para incluir contenido de publicidad en una lista de reproducción. Con los archivos de imagen y los archivos Flash que se reproducen en un bucle, también debe especificar la cantidad de tiempo que se va a mostrar el elemento multimedia incluyendo un elemento **Duration** en el elemento **ref** . Si desea que una imagen continúe mostrándose mientras se almacena en búfer la siguiente entrada de la lista de reproducción, incluya un elemento **param** en el elemento **entry** , establezca su atributo **Name** en ShowWhileBuffering y establezca su atributo **Value** en true.

Para hacer referencia al contenido de un CD o DVD que lo permita, se proporcionan los protocolos wmpcd y wmpdvd. Por ejemplo, si se establece el atributo **href** en "wmpdvd://f/5/3", se reproducirá el capítulo 3 del título 5 en un DVD, pero solo si se ha creado el DVD para permitirlo.

Las aplicaciones que abren archivos multimedia digitales desde detrás de un firewall tendrán un mejor rendimiento al abrir los elementos multimedia si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

El uso más común de este elemento es para la sustitución de direcciones URL. Si Windows Media Player no puede abrir un fragmento de medio definido en un elemento **ref** , intentará la dirección URL en el siguiente elemento **ref** . Una vez que Windows Media Player abre el contenido multimedia desde una dirección URL definida dentro del ámbito de un elemento de **entrada** , omite las siguientes etiquetas de **referencia** en el elemento de **entrada** . Una vez finalizada la reproducción de la parte del contenido, Windows Media Player pasa al siguiente elemento de **entrada** , si existe.

-   **Importante** Una vez que Windows Media Player establece una conexión a una parte de contenido a la que se hace referencia, omite todos los demás elementos **ref** de esa **entrada**, tanto si la conexión finaliza con normalidad o de forma anómala.

Si el elemento multimedia al que se hace referencia es un archivo de imagen, se debe usar el elemento **Duration** para especificar el tiempo de visualización de la imagen.

**Note**

Si intenta reproducir medios Flash que incluyen sonido con el primer fotograma, se pueden producir resultados inesperados. Debe crear contenido de Flash para reproducir el sonido a partir del segundo fotograma.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de archivos y protocolos admitidos**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





