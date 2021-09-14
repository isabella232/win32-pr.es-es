---
description: Procesamiento de datos
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Procesamiento de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160129"
---
# <a name="processing-data"></a>Procesamiento de datos

**Análisis de datos multimedia**

Si el filtro analiza los datos multimedia, no confíe en los encabezados ni en otros datos autodescriptos del contenido. Por ejemplo, no confíe en los valores de tamaño que aparecen en fragmentos avi RIFF o paquetes MPEG. Entre los ejemplos comunes de este tipo de error se incluyen:

-   Lectura *de N* bytes de datos, donde el valor de *N* provenía del contenido, sin comprobar *N* con el tamaño real del búfer.
-   Saltar a un desplazamiento de bytes dentro de un búfer, sin comprobar que el desplazamiento se encuentra dentro del búfer.

Otra clase común de errores implica no validar las descripciones de formato que se encuentran en el contenido. Por ejemplo:

-   Una [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) puede ir seguida de una tabla de colores. La **estructura BITMAPINFO** se define como una estructura **BITMAPINFOHEADER** seguida de una matriz de valores **RGBQUAD** que forma la tabla de colores. El tamaño de la matriz viene determinado por el valor de **biClrUsed.** Nunca copie una tabla de colores en **bitmapinfo** sin comprobar primero el tamaño del búfer asignado para la **estructura BITMAPINFO.**
-   Una [**estructura DESATEX**](/previous-versions/dd757713(v=vs.85)) podría tener información de formato adicional anexada a la estructura. El **miembro cbSize** especifica el tamaño de la información adicional.

Durante la conexión de anclar, un filtro debe comprobar que todas las estructuras de formato tienen el formato correcto y contienen valores razonables. Si no es así, rechace la conexión. En el código que valida la estructura de formato, tenga especial cuidado con el desbordamiento aritmético. Por ejemplo, en **un BITMAPINFOHEADER**, el ancho  y el alto son valores de 32 bits de longitud, pero el tamaño de la imagen (que es una función del producto de los dos) es solo un **valor DWORD.**

Si el formato de los datos del origen es mayor que el búfer asignado, no los trune para copiarlos en el búfer. Si lo hace, puede crear una estructura cuyo tamaño implícito sea mayor que su tamaño real. Por ejemplo, un encabezado de mapa de bits podría especificar una tabla de paleta que ya no existe. En su lugar, recate el búfer o simplemente no se puede conectar.

**Errores durante el streaming**

Cuando se ejecuta el grafo, si el filtro recibe contenido con un formato anterior, debe finalizar el streaming. Haga lo siguiente:

-   Devuelve un código de error de **Receive**.
-   Llame [**a IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el filtro de bajada.
-   Llame [**a CBaseFilter::NotifyEvent para**](cbasefilter-notifyevent.md) publicar un evento EC [**\_ ERRORABORT.**](ec-errorabort.md)

**Cambios de formato**

Existen varios mecanismos para que los filtros cambien los formatos de la secuencia media. Cada uno de ellos implica más de un paso, lo que crea la posibilidad de aceptaciones falsas. Si el filtro recibe una solicitud para un cambio de formato dinámico, debe rechazar la solicitud o, de lo contrario, respetar el nuevo formato cuando llegue. Del mismo modo, nunca cambie los formatos a menos que el otro filtro esté de acuerdo. Para obtener más información, vea [Cambios de formato dinámico.](dynamic-format-changes.md)

 

 
