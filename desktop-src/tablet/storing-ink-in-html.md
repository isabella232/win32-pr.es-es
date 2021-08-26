---
description: Normalmente, es conveniente copiar un conjunto de información más complicado de lo que se puede incluir en el formato serializado de entrada de lápiz (ISF).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Almacenamiento de entrada de lápiz en HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8949582c5743ba7be5ac664627792c7b7f8a0cd5968a67f5db08b6428cb886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934365"
---
# <a name="storing-ink-in-html"></a>Almacenamiento de entrada de lápiz en HTML

Normalmente, es conveniente copiar un conjunto de información más complicado de lo que se puede incluir en el formato serializado de entrada de lápiz (ISF). HTML es especialmente útil como formato de interoperabilidad debido a su gran aceptación como estándar del sector y su capacidad para representar contenido heterogéneo.

HTML es ampliamente comprendido, bien documentado y familiar para muchos desarrolladores. Hay muchas herramientas para la producción HTML. Además, Microsoft Windows contiene interfaces de programación de aplicaciones (API) para la representación y manipulación de HTML. Por último, las API de la plataforma de Tablet PC proporcionan el formato de persistencia GIF notificado, que es adecuado para insertar en otros formatos, lo más importante es HTML. Este formato consta de un archivo GIF con Ink Serialized Format (ISF) insertado en un bloque de extensión de aplicación.

Estos archivos GIF son representaciones de objetos de entrada de lápiz que:

-   Se representan en aplicaciones que no están habilitadas para lápiz, como exploradores o procesadores de palabras heredados.
-   Contenga toda la información necesaria de la entrada de lápiz original que se desea mantener para fines como la edición o el reconocimiento.

Estos archivos GIF se pueden generar mediante los métodos de persistencia de las API de la plataforma de Tablet PC. Son ARCHIVOS GIF y deben usar la extensión GIF y, en una aplicación que no está habilitada para la entrada de lápiz, no hay nada diferente de un GIF normal. Sin embargo, en una aplicación habilitada para lápiz hay un amplio conjunto de datos subyacentes a la imagen.

Una vez que se produce mediante las API de la plataforma de Tablet PC, se hace referencia a un GIF con notificación mediante una etiqueta IMG en HTML. A continuación, el código HTML se almacena en la ranura estándar del \_ Portapapeles CF HTML. Esto permite que el CÓDIGO HTML sea visible para otras aplicaciones, independientemente de si están habilitadas para la entrada de lápiz. La propia imagen se puede almacenar en Windows caché de Internet y establecerse en la antigüedad después de una cantidad de tiempo adecuada.

Se proporcionan o requieren adornos específicos para la etiqueta IMG. Estos adornos identifican el CÓDIGO HTML como que contiene entrada de lápiz. En el ejemplo siguiente se hace referencia a un GIF con notificación mediante etiquetas HTML:

`<img href="34372423432.gif" />`

Si es necesario hacer referencia a la imagen por otros medios, como hojas de estilos en cascada o Lenguaje de marcado de vectores (VML), todavía debe haber una etiqueta IMG que haga referencia a la imagen. Esto permite cortar y pegar dentro y fuera de cualquier aplicación que acepte representaciones HTML de lápiz.

Las aplicaciones que admiten la entrada de lápiz en HTML deben:

-   Genere CF \_ HTML cuando el usuario ejecute una copia. Al generar CF HTML en la copia (o guardar como HTML), use el método \_ [Microsoft.Ink.Ink.Save,](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) especificando el valor [Microsoft.Ink.PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) en el *parámetro p,* para generar una imagen GIF notificada. El texto alternativo debe establecerse en el resultado de reconocimiento más preciso. Puede establecer el posicionamiento en absoluto o en su lugar, según sea necesario.
-   Compruebe todas las etiquetas IMG para determinar si alguna imagen apunta a que contenga entrada de lápiz, si se elige la ranura \_ CF HTML para pegar. Si es así, trate las imágenes como [objetos ink](/previous-versions/aa515768(v=msdn.10)) internamente. Aunque solo se admiten archivos GIF en esta versión, la aplicación también debe comprobar las imágenes que no son GIF, en caso de que se admiten formatos de imagen adicionales en el futuro.
-   Admite la copia y el pegar de ISF. Las aplicaciones que admiten HTML también deben admitir ISF para mejorar la interoperabilidad con aplicaciones habilitadas para lápiz que no reconocen HTML. Esto es similar a la convención de que las aplicaciones que coloquen HTML en el Portapapeles también coloquen texto.

Para obtener más información sobre los GIF con notificaciones, vea [Bloques de creación](building-blocks.md).

 

 
