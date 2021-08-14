---
description: En este tema se enumeran los procedimientos recomendados a través de los cuales puede crear un almacén de datos basado en Windows web que se puede buscar mediante una búsqueda federada e integra los orígenes de datos remotos con Windows Explorer sin tener que escribir ni implementar ningún código del lado cliente de Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Seguir los procedimientos recomendados en Windows búsqueda federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e52d2b74f245e4ec76550cbf0a1c56b63db0a8ca6afcf9e8b736f3c7b39a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463102"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Seguir los procedimientos recomendados en Windows búsqueda federada

En este tema se enumeran los procedimientos recomendados a través de los cuales puede crear un almacén de datos basado en Windows web que se puede buscar mediante una búsqueda federada e integra los orígenes de datos remotos con Windows Explorer sin tener que escribir ni implementar ningún código del lado cliente de Windows.

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados para Windows búsqueda federada](#best-practices-for-windows-federated-search)
-   [Procedimientos recomendados para crear salidas RSS](#best-practices-for-creating-rss-output)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Procedimientos recomendados para Windows búsqueda federada

Los procedimientos recomendados [para trabajar OpenSearch](https://github.com/dewitt/opensearch) en Windows 7 son los siguientes:

-   Admita los *parámetros {startIndex}* y *{count}* y asegúrese de devolver siempre el número de elementos solicitados a menos que devuelva el último de los resultados.
-   Si conoce la extensión de nombre de archivo, asíéchala a la [propiedad System.FileExtension](../properties/props-system-fileextension.md) Windows Shell. El uso de extensiones de nombre de archivo es una manera mejor de identificar un tipo de archivo que el tipo MIME.
-   Asegúrese de que el tipo MIME o la extensión de nombre de archivo que especifique en RSS coincida con el nombre de archivo y el tipo MIME devueltos en el encabezado HTTP por el servidor web que hospeda el elemento cuando se solicita el contenido del elemento.
-   Si va a devolver elementos de archivo, devuelva un tamaño de archivo siempre que sea posible. Esto garantiza que el cuadro de diálogo progreso de la descarga sea preciso.
-   Compruebe que las solicitudes de elementos más allá del final del conjunto de resultados no devuelven ningún resultado.
    > [!Note]  
    > No repita los resultados.

     

-   No coloque etiquetas HTML a las que no pertenezcan. Según la especificación RSS, son válidas en el campo de descripción, pero no en el campo de título.
-   No cree receptáos para elementos de página web. Por ejemplo, si crea un gabinete y asigna una extensión de nombre de archivo de .aspx, el archivo se descarga mediante Windows Explorer a la caché de Internet y se ejecuta desde allí. Los exploradores web no controlan el tipo de archivo .aspx. El usuario obtenería un **Abrir con** de diálogo, o el archivo podría ser abierto por una aplicación como Microsoft Visual Studio. Evite esto devolviendo un elemento de vínculo solo para páginas web.
-   Proporcione una dirección URL de suversión web en el archivo .osdx mediante una plantilla de dirección URL con `format="text\html"` .
-   Proporcione una dirección URL a la carpeta primaria, contenedor o página web mediante la asignación de un valor de dirección URL de elemento personalizado a la propiedad [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell.

## <a name="best-practices-for-creating-rss-output"></a>Procedimientos recomendados para crear salidas RSS

Los procedimientos recomendados para crear la salida RSS son los siguientes:

-   Cada elemento DEBE devolver una dirección URL `link` `enclosure` o un valor (o equivalente, como `media:content` )
-   No incluya etiquetas de formato HTML en el atributo **title** o esas etiquetas aparecerán en el título y se mostrarán en Windows Explorer.
-   Para el **elemento description:**
    -   Muestre suficiente información para que el usuario sepa por qué este resultado podría ser relevante.
    -   No incluya formato HTML. El [OpenSearch](https://github.com/dewitt/opensearch) elimina el formato, lo que podría dar lugar a resultados inferiores a los deseados para la descripción.
    -   No incluya metadatos que ya se proporcionan en otros elementos, como el nombre del archivo de receptáu, el tamaño, la fecha de modificación, etc., porque Windows Explorer ya muestra los metadatos. Mostrarlo en el **elemento description** sería redundante.
-   Para las direcciones URL de contenido o de receptáureo:
    -   Especifique el atributo type como un tipo MIME válido.
    -   Especifique el tamaño del archivo en bytes.
-   Si va a implementar la salida RSS en .NET mediante , pruebe la fuente en Microsoft Internet Explorer para ver si es válida antes de implementarla en `DateTime` Windows Explorer.

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre cómo implementar la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, vea "Recursos adicionales" en Búsqueda federada [en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Tareas iniciales con la búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio web en Windows búsqueda federada](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en Windows búsqueda federada](-search-federated-search-data-store.md)
</dt> <dt>

[Crear un archivo OpenSearch descripción en Windows búsqueda federada](-search-federated-search-osdx-file.md)
</dt> <dt>

[Implementación de conectores de búsqueda en Windows búsqueda federada](-search-federated-search-deploying.md)
</dt> <dt>

[Extender el índice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
