---
title: Ref(Elemento)
description: El elemento REF especifica una dirección URL para el contenido multimedia digital.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070929"
---
# <a name="ref-element"></a>Ref(Elemento)

El **elemento REF** especifica una dirección URL para el contenido multimedia digital.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL a cualquier fragmento de contenido multimedia compatible con Reproductor de Windows Media.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Elementos primarios | **ENTRADA**                                                                        |
| Elementos secundarios  | **DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME** |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica una dirección URL para un fragmento de contenido multimedia. La dirección URL puede apuntar a cualquier tipo de medio admitido, mediante cualquier protocolo compatible con Reproductor de Windows Media.

Los tipos de medios admitidos incluyen imágenes fijas, como .gif y .jpg y archivos Flash con una extensión de nombre de archivo .jpeg. Estos tipos de medios son útiles para incluir contenido de publicidad dentro de una lista de reproducción. Con los archivos de imagen y los archivos Flash que se reproducen en un bucle, también debe especificar la cantidad de tiempo para mostrar el elemento multimedia mediante la inclusión de un elemento **DURATION** dentro del **elemento REF.** Si quiere que una imagen siga mostrándose mientras se almacena en búfer la siguiente entrada  de la lista de reproducción,  incluya un elemento **PARAM** dentro del elemento **ENTRY,** establezca su atributo name en ShowWhileBuffering y establezca su atributo value en true.

Para hacer referencia al contenido de un CD o DVD que lo permita, se proporcionan los protocolos wmpcd y wmpdvd. Por ejemplo, si se establece el atributo **HREF** en "wmpdvd://f/5/3", se reproducirá el capítulo 3 del título 5 en un DVD, pero solo si se ha escrito el DVD para permitirlo.

Las aplicaciones que abren medios digitales desde detrás de un firewall tendrán un mejor rendimiento al abrir los elementos multimedia si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

El uso más común de este elemento es para la suversión de direcciones URL. Si Reproductor de Windows Media no puede abrir un elemento multimedia definido en un elemento **REF,** prueba la dirección URL en el siguiente **elemento REF.** Una Reproductor de Windows Media abre el contenido multimedia desde una dirección URL definida dentro del ámbito de un **elemento ENTRY,** omite las etiquetas **REF** posteriores dentro de **ese elemento ENTRY.** Una vez que el elemento de contenido haya terminado de reproducirse, Reproductor de Windows Media pasa al siguiente elemento **ENTRY,** si existe.

-   **Importante** Una Reproductor de Windows Media establece una conexión a un fragmento de contenido al que se hace referencia, omite todos los demás elementos **REF** de ese **ENTRY,** tanto si la conexión finaliza de forma normal como anómala.

Si el elemento multimedia al que se hace referencia es un archivo de imagen, el elemento **DURATION** debe usarse para especificar la hora de presentación de la imagen.

**Nota**

Intentar reproducir medios Flash que incluyan sonido con el primer fotograma puede producir resultados inesperados. Debe crear contenido flash para reproducir el sonido a partir del segundo fotograma.

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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Protocolos y tipos de archivo admitidos**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





