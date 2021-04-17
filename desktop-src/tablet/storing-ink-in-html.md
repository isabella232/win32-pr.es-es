---
description: Normalmente, es deseable copiar un conjunto de información más complicado del que se puede incluir en el formato serializado de tinta (ISF).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Almacenar entradas manuscritas en HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372e6e77ea0284bc44fa70883964e53b3063bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678190"
---
# <a name="storing-ink-in-html"></a>Almacenar entradas manuscritas en HTML

Normalmente, es deseable copiar un conjunto de información más complicado del que se puede incluir en el formato serializado de tinta (ISF). HTML es especialmente útil como un formato de interoperabilidad debido a su aceptación fuerte como un estándar del sector y su capacidad de representar contenido heterogéneo.

HTML está ampliamente entendido, está bien documentado y está familiarizado con muchos desarrolladores. Hay muchas herramientas para la producción en HTML. Además, Microsoft Windows contiene interfaces de programación de aplicaciones (API) para la representación y manipulación de HTML. Por último, las API de la plataforma de Tablet PC proporcionan el formato de persistencia GIF enriquecido, que es adecuado para la inserción en otros formatos, lo que es más importante en HTML. Este formato consta de un archivo GIF con el formato serializado de tinta (ISF) incrustado en un bloque de extensión de aplicación.

Estos archivos GIF son representaciones de objetos de entrada de lápiz que:

-   Se representan en aplicaciones que no están habilitadas para tinta, como exploradores o procesadores de textos heredados.
-   Contenga toda la información necesaria de la tinta original que desea mantener con fines como la edición o el reconocimiento.

Estos archivos GIF se pueden generar mediante los métodos de persistencia de las API de la plataforma de Tablet PC. Son archivos GIF y deben usar la extensión GIF y, en una aplicación que no está habilitada para la entrada de lápiz, no hay nada diferente de los GIF normales. Sin embargo, en una aplicación con tinta habilitada hay un conjunto completo de datos subyacentes de la imagen.

Una vez generadas por las API de la plataforma de Tablet PC, se hace referencia a un GIF enriquecido mediante una etiqueta IMG en HTML. El código HTML se almacena en la ranura del \_ portapapeles HTML de CF estándar. Esto permite que el código HTML esté visible para otras aplicaciones, independientemente de si están habilitados para la entrada de lápiz. La propia imagen se puede almacenar en la caché de Internet de Windows y establecer para que caduque después de un período de tiempo adecuado.

Se proporcionan elementos gráficos específicos a la etiqueta IMG o son necesarios. Estos elementos gráficos identifican el código HTML que contiene la tinta. En el ejemplo siguiente se hace referencia a un GIF enriquecido mediante etiquetas HTML:

`<img href="34372423432.gif" />`

Si es necesario hacer referencia a la imagen por otros medios, como hojas de estilos en cascada o Lenguaje de marcado de vectores (VML), debería haber todavía una etiqueta IMG que haga referencia a la imagen. Esto permite cortar y pegar dentro y fuera de cualquier aplicación que acepte representaciones HTML de tinta.

Las aplicaciones que admiten la entrada manuscrita en HTML deberían:

-   Genere \_ el código HTML de CF cuando el usuario ejecute una copia. Al generar el \_ HTML CF al copiar (o guardar como HTML), use el método [Microsoft. Ink. Ink. Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) , especificando el valor [Microsoft. Ink. PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) en el parámetro *p* , para generar una imagen GIF enriquecida. El texto alternativo debe establecerse en el resultado de reconocimiento más preciso. Puede establecer la posición en absoluta o en contexto, según sea necesario.
-   Marque todas las etiquetas IMG para determinar si las imágenes que señalan contienen tinta, si \_ se elige la ranura HTML de CF para pegar. Si es así, trate las imágenes como objetos de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) internamente. Aunque solo se admiten archivos GIF en esta versión, la aplicación debe comprobar también las imágenes no GIF, en caso de que se admitan formatos de imagen adicionales en el futuro.
-   Admite la copia y el pegado del ISF. Las aplicaciones que admiten HTML también deben admitir ISF para mejorar la interoperabilidad con aplicaciones habilitadas para tinta que no reconocen HTML. Esto es similar a la Convención de que las aplicaciones que colocan HTML en el portapapeles también colocan texto.

Para obtener más información sobre los archivos GIF enriquecidos, vea [bloques de creación](building-blocks.md).

 

 
