---
title: Creación de listas de reproducción de metarchivo
description: Creación de listas de reproducción de metarchivo
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Listas de reproducción de metarchivos multimedia, creación
- listas de reproducción, crear
- listas de reproducción de metarchivo, crear
- crear listas Windows de metarchivo multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 765d8ab507c2ce502f1cad021696b0fc2ecfd110da8dfa95ccc84a43a8987561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750472"
---
# <a name="creating-metafile-playlists"></a>Creación de listas de reproducción de metarchivo

Puede crear una lista de reproducción mediante cualquier editor de texto, como Microsoft Bloc de notas. Abra el editor de texto. Escriba las entradas de script que desea implementar. Cuando haya terminado de escribir en Bloc de notas, guarde el archivo con un nombre de archivo y una extensión de nombre de archivo adecuados. Para obtener más información sobre las extensiones, vea [Metafile Extension Guidelines](metafile-extension-guidelines.md). Normalmente, el nombre de archivo es el nombre del archivo o secuencia de Windows Media seguido de una extensión de .locución, .wvx o .asx. Por ejemplo, si el contenido multimedia es un archivo de audio multimedia Windows que tiene una extensión .wma, use la extensión .extension al asignar un nombre a la lista de reproducción. Las listas de reproducción no deben incluir ningún código de formato de un procesador de textos, como Microsoft Word. Para asegurarse de que no se incluyen códigos de formato en la lista de reproducción, guarde el archivo como un archivo ASCII o de texto sin formato.

> [!Note]  
> Los elementos y atributos no distinguen mayúsculas de minúsculas. El texto usado en la lista de reproducción para definir un elemento o atributo puede estar en mayúsculas o minúsculas, o bien una combinación de ambos.

 

Si un elemento no tiene ningún elemento secundario (los que modifican o están contenidos dentro de otro elemento), se puede usar un carácter de barra diagonal única (/) al final de la etiqueta de apertura, justo antes del ">", en lugar de una etiqueta de cierre. Los elementos secundarios de un elemento deben aparecer entre la etiqueta de apertura y cierre de ese elemento; De lo contrario, no son elementos secundarios para ese elemento y se omiten o provocan un error en la sintaxis de la lista de reproducción.

Los cuatro primeros caracteres de una lista de reproducción deben ser &lt; "ASX". El **elemento ASX** se usa en todas las listas de reproducción, independientemente de si su extensión es .desenlace, .wvx o .asx. Solo debe haber un elemento **ASX** por lista de reproducción. Este elemento identifica el archivo como una lista de reproducción Windows metarchivo multimedia. No especifica el tipo de lista de reproducción.

El **elemento ASX** tiene tres atributos posibles:

**VERSION**

El **atributo VERSION** es necesario y debe seguir inmediatamente después del elemento **ASX,** por ejemplo, "<versión de ASX = "3.0" &gt; ". El número de versión actual es 3.0. Reproductor de Windows Media admite todas las versiones anteriores. Los valores aceptables para **el atributo VERSION** incluyen 3.0 y 3 (sin separador decimal).

**PREVIEWMODE**

El **atributo PREVIEWMODE** es opcional. Proporciona otro mecanismo para especificar cuánto tiempo se va a representar un clip. Si el valor del atributo **PREVIEWMODE** es YES, Reproductor de Windows Media cada clip durante la duración especificada por el **elemento PREVIEWDURATION**. Cada clip puede tener **un valor PREVIEWDURATION** especificado.

**BANNERBAR**

El atributo **BANNERBAR** opcional define si el control Reproductor de Windows Media reserva espacio para un gráfico de banner. (Use el **elemento BANNER** para especificar el gráfico que se mostrará). Si el valor de **BANNERBAR** es FIXED, Reproductor de Windows Media reserva espacio para el banner para el show y para cada clip, si la lista de reproducción de metarchivo especifica un banner para el show o clip. Esto mantendrá el tamaño de la ventana de Reproductor de Windows Media igual (excepto cuando cambia el tamaño del vídeo) independientemente de la ausencia o la presencia de un gráfico de banner. Si el clip o la presentación no tienen un banner asociado, el espacio reservado para uno es negro. Si el valor del atributo **BANNERBAR** es AUTO, Reproductor de Windows Media reserva espacio para el banner solo cuando el clip o la presentación incluyen uno.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Para obtener más información sobre los tres atributos del **elemento ASX,** vea la entrada de referencia para el [elemento ASX](asx-element.md).

Un **elemento ASX** contiene **elementos secundarios ENTRY** que definen información sobre los archivos multimedia a los que se va a tener acceso. Cada **elemento ENTRY** debe contener un elemento **REF** que especifique la ruta de acceso al archivo multimedia que se va a transmitir. Debe haber al menos un **elemento ENTRY** **o ENTRYREF** dentro de un **elemento ASX.**

Otros elementos definidos dentro del ámbito del elemento **ASX,** como **TITLE** y **AUTHOR**, están asociados a los metadatos mostrados por Reproductor de Windows Media.

Las listas de reproducción más sencillas se crean agregando varios **elementos ENTRY** con un único **elemento REF** a un metarchivo. Cada **elemento ENTRY** de una lista de reproducción de metarchivo se representa en el orden en que aparece en el archivo como si el usuario hubiera abierto manualmente cada clip.

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



Asegúrese de que la lista de reproducción funciona haciendo doble clic en ella en Windows Explorador. Reproductor de Windows Media abrir y empezar a transmitir el contenido multimedia. Una vez que haya confirmado que la lista de reproducción funciona, guárdela en el servidor web junto con las páginas web y vincórela a ella mediante un **elemento HREF,** o insórrela en una página web mediante el elemento **Reproductor de Windows Media OBJECT.**

Las secciones siguientes contienen más información:

-   [Anidamiento de metarchivos](nesting-metafiles.md)
-   [Uso de asp pages para crear dinámicamente listas Windows de metarchivo multimedia](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento BANNER**](banner-element.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




