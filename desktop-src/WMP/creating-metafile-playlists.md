---
title: Crear listas de reproducción de metarchivo
description: Crear listas de reproducción de metarchivo
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Listas de reproducción de metarchivos de Windows Media, crear
- listas de reproducción, crear
- listas de reproducción de metarchivos, crear
- crear listas de reproducción de metarchivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269127"
---
# <a name="creating-metafile-playlists"></a>Crear listas de reproducción de metarchivo

Puede crear una lista de reproducción mediante cualquier editor de texto, como el Bloc de notas de Microsoft. Abra el editor de texto. Escriba las entradas de script que desea implementar. Una vez que haya terminado de escribir en el Bloc de notas, guarde el archivo con un nombre de archivo y una extensión de nombre de archivo apropiados. Para obtener más información acerca de las extensiones, consulte [instrucciones de extensión de metarchivo](metafile-extension-guidelines.md). Normalmente, el nombre de archivo es el nombre del archivo o secuencia de Windows Media seguido de una extensión de. Wax,. wvx o. ASX. Por ejemplo, si el contenido multimedia es un archivo de audio de Windows Media con la extensión. WMA, use la extensión. Wax al asignar un nombre a la lista de reproducción. Las listas de reproducción no deben incluir códigos de formato de un procesador de textos, como Microsoft Word. Para asegurarse de que no se incluyen códigos de formato en la lista de reproducción, guarde el archivo como texto sin formato o como archivo ASCII.

> [!Note]  
> Los elementos y los atributos no distinguen mayúsculas de minúsculas. El texto que se utiliza en la lista de reproducción para definir un elemento o un atributo puede estar en mayúsculas o en minúsculas, o bien una combinación de ambos.

 

Si un elemento no tiene elementos secundarios (los que modifican o están contenidos en otro elemento), se puede usar un carácter de barra diagonal (/) al final de la etiqueta de apertura, justo antes de la ' > ', en lugar de una etiqueta de cierre. Los elementos secundarios de un elemento deben aparecer entre la etiqueta de apertura y el cierre de ese elemento; de lo contrario, no son elementos secundarios de ese elemento y se omiten o causan un error en la sintaxis de la lista de reproducción.

Los cuatro primeros caracteres de una lista de reproducción deben ser " &lt; ASX". El elemento **ASX** se usa en todas las listas de reproducción si su extensión es. Wax,. wvx o. ASX. Solo debe haber un elemento **ASX** por cada lista de reproducción. Este elemento identifica el archivo como una lista de reproducción de metarchivo de Windows Media. No especifica el tipo de lista de reproducción.

El elemento **ASX** tiene tres atributos posibles:

**VERSION**

El atributo **version** es necesario y debe seguir inmediatamente después del elemento **ASX** , por ejemplo "<ASX version =" 3,0 " &gt; ". El número de versión actual es 3,0. Windows Media Player es compatible con todas las versiones anteriores. Los valores aceptables para el atributo **version** incluyen 3,0 y 3 (sin separador decimal).

**PREVIEWMODE**

El atributo **PREVIEWMODE** es opcional. Proporciona otro mecanismo para especificar cuánto tiempo se debe representar un clip. Si el valor del atributo **PREVIEWMODE** es Yes, Windows Media Player representará cada clip durante la duración especificada por el elemento **PREVIEWDURATION**. Cada clip puede tener un **PREVIEWDURATION** especificado.

**BANNERBAR**

El atributo **BANNERBAR** opcional define si el control de Media Player de Windows Reserva espacio para un gráfico de banner. (Use el elemento **banner** para especificar el gráfico que se va a mostrar). Si el valor de **BANNERBAR** es fijo, Windows Media Player reserva el espacio de banner para la presentación y para cada clip, independientemente de si la lista de reproducción del metarchivo especifica un banner para el programa o el clip. Esto hará que el tamaño de la ventana de Media Player de Windows sea el mismo (excepto cuando el tamaño del vídeo cambie) independientemente de la ausencia o la presencia de un gráfico de banner. Si el programa o el clip no tienen un encabezado asociado, el espacio reservado para uno es negro. Si el valor del atributo **BANNERBAR** es auto, Windows Media Player Reserva espacio para el banner solo cuando el programa o el clip incluye uno.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Para obtener más información sobre los tres atributos del elemento **ASX** , vea la entrada de referencia para el [elemento ASX](asx-element.md).

Un elemento **ASX** contiene elementos secundarios **entry** que definen información sobre los archivos multimedia a los que se va a obtener acceso. Cada elemento **entry** debe contener un elemento **ref** que especifique la ruta de acceso al archivo multimedia que se va a transmitir. Debe haber al menos un elemento **entry** o **ENTRYREF** dentro de un elemento **ASX** .

Otros elementos definidos dentro del ámbito del elemento **ASX** , como **title** y **Author**, se asocian con los metadatos que muestra Windows Media Player.

Las listas de reproducción más sencillas se crean agregando varios elementos de **entrada** con un solo elemento **ref** a un metarchivo. Cada elemento de **entrada** de una lista de reproducción de metarchivo se representa en el orden en que aparece en el archivo como si el usuario hubiera abierto manualmente cada clip.

Código de ejemplo


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



Asegúrese de que la lista de reproducción funcione haciendo doble clic en él en el explorador de Windows. Windows Media Player debe abrir y comenzar a transmitir por secuencias el contenido multimedia. Una vez que haya confirmado que la lista de reproducción funciona, guárdela en el servidor web junto con las páginas web y vincúlela por medio de un elemento **href** o insértela en una página web mediante el elemento de **objeto** Windows Media Player.

Las secciones siguientes contienen más información:

-   [Anidar metaarchivos](nesting-metafiles.md)
-   [Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




