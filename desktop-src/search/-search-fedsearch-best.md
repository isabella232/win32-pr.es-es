---
description: En este tema se enumeran los procedimientos recomendados a través de los que puede crear un almacén de datos basado en Web que se puede buscar mediante la búsqueda federada de Windows e integrar los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Siguientes procedimientos recomendados en la búsqueda federada de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153975"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Siguientes procedimientos recomendados en la búsqueda federada de Windows

En este tema se enumeran los procedimientos recomendados a través de los que puede crear un almacén de datos basado en Web que se puede buscar mediante la búsqueda federada de Windows e integrar los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.

Este tema se organiza de la siguiente manera:

-   [Prácticas recomendadas para la búsqueda federada de Windows](#best-practices-for-windows-federated-search)
-   [Prácticas recomendadas para crear una salida RSS](#best-practices-for-creating-rss-output)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Prácticas recomendadas para la búsqueda federada de Windows

Los procedimientos recomendados para trabajar con [OpenSearch](https://github.com/dewitt/opensearch) en Windows 7 son los siguientes:

-   Admita los parámetros *{startIndex}* y *{Count}* y asegúrese de devolver siempre el número de elementos solicitados a menos que devuelva el último de los resultados.
-   Si conoce la extensión de nombre de archivo, asígnela a la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) . El uso de extensiones de nombre de archivo es una manera mejor de identificar un tipo de archivo que el tipo MIME.
-   Asegúrese de que el tipo MIME o la extensión de nombre de archivo que especifique en el RSS coincide con el nombre de archivo y el tipo MIME devuelto en el encabezado HTTP por el servidor Web que hospeda el elemento cuando se solicita el contenido del elemento.
-   Si va a devolver elementos de archivo, devuelva un tamaño de archivo siempre que sea posible. Esto garantiza que el cuadro de diálogo progreso de la descarga sea preciso.
-   Compruebe que las solicitudes de elementos que van más allá del final del conjunto de resultados no devuelven resultados.
    > [!Note]  
    > No repetir resultados.

     

-   No coloque etiquetas HTML a las que no pertenezcan. Según la especificación RSS, son válidas en el campo Descripción, pero no en el campo título.
-   No cree contenedores para los elementos de la Página Web. Por ejemplo, si crea un contenedor y asigna una extensión de nombre de archivo. aspx, el explorador de Windows descarga el archivo en la memoria caché de Internet y se ejecuta desde allí. Los exploradores Web no controlan el tipo de archivo. aspx. El usuario obtenería un cuadro **de diálogo Abrir con** o un archivo podría estar abierto por una aplicación como Microsoft Visual Studio. Evite esto devolviendo un elemento de vínculo solo para las páginas Web.
-   Proporcione una dirección URL de sustitución Web en el archivo. osdx con una plantilla de dirección URL con `format="text\html"` .
-   Proporcione una dirección URL a la carpeta principal, el contenedor o la página web asignando un valor de dirección URL de elemento personalizado a la propiedad del shell de Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .

## <a name="best-practices-for-creating-rss-output"></a>Prácticas recomendadas para crear una salida RSS

Los procedimientos recomendados para crear la salida RSS son los siguientes:

-   Cada elemento debe devolver una dirección URL `link` o un `enclosure` valor (o equivalente, como `media:content` )
-   No incluya etiquetas de formato HTML en el atributo de **título** , o esas etiquetas aparecerán en el título y se mostrarán en el explorador de Windows.
-   Para el elemento **Description** :
    -   Mostrar información suficiente para que el usuario sepa por qué este resultado podría ser pertinente.
    -   No incluya formato HTML. El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) quita el formato, lo que puede dar lugar a resultados menores que los deseados para la descripción.
    -   No incluya metadatos que ya se hayan proporcionado en otros elementos, como nombre de archivo de contenedor, tamaño, fecha de modificación, etc., porque el explorador de Windows ya muestra los metadatos. Mostrarlo en el elemento de **Descripción** sería redundante.
-   Para las direcciones URL de contenido o contenedor:
    -   Especifique el atributo type como un tipo MIME válido.
    -   Especifique el tamaño del archivo en bytes.
-   Si va a implementar la salida RSS en .NET mediante `DateTime` , pruebe la fuente en Microsoft Internet Explorer para ver si es válida antes de implementarla en el explorador de Windows.

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introducción con búsqueda federada en Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conexión del servicio Web en la búsqueda federada de Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitación del almacén de datos en la búsqueda federada de Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creación de un archivo de descripción de OpenSearch en Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Implementación de conectores de búsqueda en la búsqueda federada de Windows](-search-federated-search-deploying.md)
</dt> <dt>

[Extender el índice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
