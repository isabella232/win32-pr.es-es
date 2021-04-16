---
description: Procesamiento de datos
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Procesamiento de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677147"
---
# <a name="processing-data"></a>Procesamiento de datos

**Analizar datos multimedia**

Si el filtro analiza datos multimedia, no confíe en encabezados u otros datos autodescriptivos en el contenido. Por ejemplo, no confíe en los valores de tamaño que aparecen en fragmentos o paquetes MPEG RIFF de AVI. Algunos ejemplos comunes de este tipo de error son:

-   Lectura de *n* bytes de datos, donde el valor de *n* procedía del contenido, sin comprobar si el tamaño real del búfer *es n.*
-   Saltar a un desplazamiento de bytes dentro de un búfer, sin comprobar que el desplazamiento está dentro del búfer.

Otra clase común de errores implica no validar las descripciones de formato que se encuentran en el contenido. Por ejemplo:

-   Una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) puede ir seguida de una tabla de colores. La estructura **bitmapinfo (** se define como una estructura **BITMAPINFOHEADER** seguida de una matriz de valores **RGBQUAD** que forman la tabla de colores. El tamaño de la matriz viene determinado por el valor de **biClrUsed**. Nunca copie una tabla de colores en un **bitmapinfo (** sin comprobar primero el tamaño del búfer que se asignó para la estructura **bitmapinfo (** .
-   Una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) podría tener información de formato adicional anexada a la estructura. El miembro **cbSize** especifica el tamaño de la información adicional.

Durante la conexión de PIN, un filtro debe comprobar que todas las estructuras de formato tienen el formato correcto y contienen valores razonables. Si no es así, rechace la conexión. En el código que valida la estructura de formato, preste especial atención al desbordamiento aritmético. Por ejemplo, en un **BITMAPINFOHEADER**, el ancho y el alto son valores **largos** de 32 bits, pero el tamaño de la imagen (que es una función del producto de los dos) solo es un valor **DWORD** .

Si el formato de los datos de origen es mayor que el búfer asignado, no trunque los datos de origen para copiarlos en el búfer. Si lo hace, puede crear una estructura cuyo tamaño implícito sea mayor que su tamaño real. Por ejemplo, un encabezado de mapa de bits podría especificar una tabla de paleta que ya no existe. En su lugar, reasigne el búfer o simplemente genere un error en la conexión.

**Errores durante el streaming**

Cuando el gráfico se está ejecutando, si el filtro recibe contenido incorrecto, debe terminar la transmisión por secuencias. Haga lo siguiente:

-   Devuelve un código de error de **Receive**.
-   Llame a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el filtro de nivel inferior.
-   Llame a [**CBaseFilter:: NotifyEvent**](cbasefilter-notifyevent.md) para publicar un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) .

**Cambiar formato**

Existen varios mecanismos para que los filtros cambien los formatos a la secuencia intermedia. Cada una de ellas implica más de un paso, lo que crea el potencial para aceptaciones falsas. Si el filtro recibe una solicitud de cambio de formato dinámico, debe rechazar la solicitud, o bien respetar el nuevo formato cuando llegue. De igual forma, nunca cambie los formatos a menos que el otro filtro acepte. Para obtener más información, consulte [Dynamic Format Changes](dynamic-format-changes.md).

 

 
