---
title: Usar vínculos relativos en los metaarchivos
description: Usar vínculos relativos en los metaarchivos
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Listas de reproducción de metarchivos de Windows Media, vínculos relativos
- listas de reproducción, vínculos relativos
- listas de reproducción de metarchivos, vínculos relativos
- metaarchivos, vínculos relativos
- Metaarchivos de Windows Media, vínculos relativos
- vínculos relativos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903323"
---
# <a name="using-relative-links-in-metafiles"></a>Usar vínculos relativos en los metaarchivos

Los vínculos relativos son una característica totalmente compatible de los metaarchivos de Windows Media. Puede usar vínculos relativos en los metaarchivos de forma muy parecida a como se usan en documentos HTML. El uso de vínculos relativos le permite crear metarchivos que son portátiles, lo que significa que puede copiar o mover una estructura de directorios completa a otro servidor sin actualizar las rutas de acceso a los archivos de gráficos usados como pancartas o los atributos **href** de los elementos **MOREINFO** (si hacen referencia a archivos en el mismo servidor Web que el metarchivo almacenado). Los vínculos relativos funcionan, en cualquier aplicación que los admita, porque las partes de la dirección URL que no están incluidas en el atributo **href** de un elemento se incluyen en la dirección URL enviada por la aplicación al servidor cuando se solicita esa dirección URL. Esto significa que el protocolo (como https://), el nombre del servidor y el directorio virtual en el que se encuentra el archivo que contiene el vínculo relativo están incluidos en la dirección URL que se envía al servidor. Si el archivo multimedia o la dirección URL a la que se vincula mediante un vínculo relativo no residen en el mismo servidor que el metarchivo, el vínculo relativo no es válido.

> [!Note]  
> Esta información sobre vínculos relativos solo es correcta cuando se usa un vínculo a los metaarchivos que se abren en el Media Player de Windows independiente. Cuando se usa el control Embedded Windows Media Player, todos los vínculos son relativos a la página en la que se hospeda el control, a menos que se use el elemento secundario **base** del elemento **ASX** para redirigir la ruta de acceso relativa.

 

Todos los vínculos relativos del metarchivo deben ser totalmente relativos, no relativos a la unidad, para los medios de streaming. Cuando una dirección URL comienza con un \\ carácter "", el vínculo es relativo a la unidad. Windows Media Player intenta abrir el archivo vinculado a en la unidad en la que se abrió el metarchivo, normalmente un servidor Web. Dado que los servidores web usan directorios virtuales, Windows Media Player intenta encontrar el flujo especificado o el archivo multimedia en un subdirectorio de un directorio virtual del servidor web desde el que se abrió el metarchivo. Un usuario no tendría acceso a un directorio del servidor. En el ejemplo de esta sección se muestra el uso de un vínculo totalmente relativo.

Puede usar vínculos relativos a unidades de disco al usar metaarchivos en un único equipo en el que todos los archivos multimedia a los que se ha vinculado en la lista de reproducción del metarchivo existen en un dispositivo de almacenamiento de ese equipo. Sin embargo, no puede transmitir multimedia de esta manera.

Cuando se usa un vínculo a otro metarchivo para permitir vínculos relativos, el nombre mostrado como título por Windows Media Player es el título del metarchivo original.

Los vínculos relativos no se pueden usar para las direcciones URL en un servidor de streaming multimedia porque se usan protocolos diferentes para tener acceso al contenido multimedia de streaming.

En la lista de reproducción de ejemplo siguiente, el primer **ENTRYREF** contiene una dirección URL para otra lista de reproducción, relative. Wax.


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



El siguiente ejemplo es el archivo relative. Wax, que contiene vínculos relativos.


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



La dirección URL que contiene la referencia a la lista de reproducción, relative. Wax, puede existir en una lista de reproducción de metarchivo en cualquier lugar que sea accesible para el usuario. Para que la dirección URL se procese correctamente, debe haber un servidor Web denominado "example.microsoft.com". Ese servidor Web debe tener un directorio virtual definido como "Metafiles". La lista de reproducción a la que se hace referencia, relative. Wax, debe existir en el servidor Web denominado "example.microsoft.com" en el directorio virtual "Metafiles".

En el caso de los archivos multimedia a los que se hace referencia en la lista de reproducción relativa. Wax para tener acceso y reproducirse correctamente, debe haber un directorio denominado "Graphics", que es un subdirectorio del directorio virtual del servidor "Metafiles". El archivo de gráficos Logo1.jpg, al que se hace referencia en el elemento **banner** , debe ser el subdirectorio denominado Graphics.

Del mismo modo, un documento denominado Category1.htm debe residir en un subdirectorio denominado Category1. El directorio denominado Category1 debe existir como subdirectorio del directorio virtual "Metafiles" en el servidor Web example.microsoft.com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




