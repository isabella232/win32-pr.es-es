---
description: En este tema se describen las tres fases del proceso de indización y los componentes principales implicados en cada una de ellas, se explica el tiempo de la actividad de indización y se proporcionan algunas notas para los desarrolladores de terceros que desean que sus almacenes de datos o formatos de archivo se indexen.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Proceso de indexación en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87867d5925cd53b237092435bbc9d16428418b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808953"
---
# <a name="indexing-process-in-windows-search"></a>Proceso de indexación en Windows Search

En este tema se describen las tres fases del proceso de indización y los componentes principales implicados en cada una de ellas, se explica el tiempo de la actividad de indización y se proporcionan algunas notas para los desarrolladores de terceros que desean que sus almacenes de datos o formatos de archivo se indexen.

Este tema se organiza de la siguiente manera:

- [Información general](#overview)
- [Fase 1: poner en cola las direcciones URL para la indexación](#stage-1-queuing-urls-for-indexing)
- [Fase 2: rastreo de direcciones URL](#stage-2-crawling-urls)
- [Fase 3: actualización del índice](#stage-3-updating-the-index)
- [Cómo se programa la indexación](#how-indexing-is-scheduled)
- [Notas a los implementadores](#notes-to-implementers)
- [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Windows Search admite la indización de propiedades y contenido de archivos de distintos formatos de archivo, como formatos. doc o. JPEG, y almacenes de datos, como el sistema de archivos o los buzones de correo de Windows Outlook. Hay dos tipos de índices: índices de valor que permiten filtrar y ordenar por el valor completo de una propiedad y índices invertidos que indexan palabras dentro de las propiedades de texto o el contenido. Si tiene un formato de archivo personalizado o un almacén de datos, debe comprender el modo en que los índices de búsqueda de Windows permiten que los elementos se indexen correctamente.

El proceso de indización se produce en tres fases controladas por un componente de búsqueda de Windows denominado recopilador. En la primera fase, el recopilador agrega direcciones URL a las colas. Las direcciones URL identifican los elementos que se van a indexar, y las colas simplemente tienen prioridad en las listas de direcciones URL. En la segunda fase, el recopilador coordina otros componentes de búsqueda de Windows y de terceros para tener acceso a los elementos y recopilar datos sobre ellos. Por último, en la tercera fase, los datos recopilados se agregan al índice.

En el diagrama siguiente se muestran los componentes principales y el flujo de datos a través del proceso de indización. Hay varios componentes implicados en la recopilación de datos para el índice. Algunos de ellos forman parte de la búsqueda de Windows y otros proceden de aplicaciones de terceros. Si tiene un almacén de datos o un formato de archivo personalizado, la búsqueda de Windows se basa en el controlador de protocolo y filtra el acceso a las direcciones URL y la emisión de propiedades para la indexación. Los componentes de Windows Search se muestran en azul y los componentes de terceros se muestran en verde.

![diagrama que muestra la interacción entre los componentes durante el proceso de indexación](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Fase 1: poner en cola las direcciones URL para la indexación

En la primera fase de la indización, el recopilador recopila información sobre las actualizaciones de los almacenes de datos, compara esa información con el ámbito de rastreo conocido y, a continuación, crea una cola de direcciones URL para atravesar para recopilar datos para el índice. En el caso de los orígenes que no se basan en la notificación, como unidades FAT, el recopilador inicia periódicamente un recorrido completo del ámbito de rastreo para que los datos del índice se mantengan actualizados. En el caso de orígenes como NTFS, solo hay un rastreo y todo lo demás lo controlan las notificaciones del [diario de cambios de USN](/windows/desktop/FileIO/change-journals). Tampoco hay ningún rastreo de Microsoft Outlook. En el diagrama siguiente se muestra una vista de alto nivel del proceso de puesta en cola para la indexación sin rastreo.

![diagrama que muestra el proceso de consulta para la indización que no es de rastreo](images/queuingurls.jpg)

En el resto de esta sección se explica cómo la búsqueda de Windows determina las direcciones URL que se van a rastrear y se definen algunos términos importantes durante el proceso.

**Ámbito de rastreo**  El ámbito de rastreo es un conjunto de direcciones URL que la búsqueda de Windows atraviesa para recopilar datos acerca de los elementos que el usuario quiere indexar para búsquedas más rápidas. Windows Search agrega algunas direcciones URL al ámbito de rastreo de forma predeterminada, como las rutas de acceso a las carpetas de **documentos** e **imágenes** de los usuarios. Otras aplicaciones, usuarios y directiva de grupo pueden agregar otras direcciones URL. Por último, los usuarios y directiva de grupo pueden excluir explícitamente las direcciones URL. Windows Search toma todas las direcciones URL agregadas y quita las direcciones URL excluidas para determinar el ámbito de rastreo. Este es el espacio de trabajo de las direcciones URL desde las que el recopilador comienza su trabajo.

**Recopilador**  El recopilador es un componente de Windows Search que recopila información sobre las direcciones URL del ámbito de rastreo y crea una cola de direcciones URL para que el indizador rastree. Cuando se agrega, elimina o actualiza un elemento en el ámbito de rastreo, el proveedor de notificaciones del almacén de datos notifica al recopilador. Hay un rastreo inicial en el que el recopilador comienza en la raíz del ámbito de rastreo. La dirección URL se pasa al controlador de protocolo y, a continuación, al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)adecuado. El filtro suele ser una enumeración de directorios que genera más direcciones URL. Las notificaciones son el estado estable. Normalmente, cada almacén de datos tiene su propio controlador de protocolo que proporciona estas notificaciones. Por ejemplo, en el sistema de archivos local, el [diario de cambios USN](/windows/desktop/FileIO/change-journals) actúa como proveedor de notificaciones para todas las direcciones URL del protocolo File://. De forma similar, Microsoft Outlook actúa como proveedor de notificaciones para todas las direcciones URL del protocolo mapi://. Cuando un usuario recibe, mueve o elimina el correo electrónico, Outlook notifica al recopilador el estado cambiado del correo electrónico. Desde estas notificaciones, el recopilador crea colas de indexación de las direcciones URL que se van a rastrear.

**Indexación de colas**  Las colas de indexación son listas de direcciones URL que identifican los elementos que se deben indexar o volver a indexar. El recopilador compara las direcciones URL que recibe de los proveedores de notificaciones con las direcciones URL del ámbito de rastreo. Cada dirección URL de los proveedores de notificaciones que se encuentra dentro del ámbito de rastreo se agrega a una cola que el recopilador utiliza para dar prioridad a las direcciones URL que se van a procesar a continuación.

Hay tres colas: notificaciones de prioridad alta, notificaciones normales y rastreos periódicos. La cola de prioridad alta es para las notificaciones que se deben procesar inmediatamente. Por ejemplo, cuando un usuario cambia la propiedad título de un elemento en el explorador de Windows, la vista del explorador de Windows debe actualizarse inmediatamente después del cambio. La cola de notificación normal es para todas las notificaciones de cambio restantes. Las colas de notificaciones se procesan antes que la cola de rastreo porque es más probable que los elementos modificados sean de interés para un usuario. El recopilador obtiene acceso a los datos de las direcciones URL de cada cola en orden FIFO (primero en salir, primero en salir).

Para obtener más información sobre la priorización y las API de eventos que se introdujeron en Windows 7, consulte [indización de los eventos Priority y Rowset en Windows 7](indexing-prioritization-and-rowset-events.md). Para obtener más información sobre la administración del ámbito de rastreo y las notificaciones, vea [proporcionar notificaciones de cambio](-search-3x-wds-notifyingofchanges.md) y [usar el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Fase 2: rastreo de direcciones URL

En la segunda fase de la indización, el recopilador rastrea las colas, el acceso a los almacenes de datos y la recuperación de secuencias de elementos. En primer lugar, el recopilador busca el controlador de protocolo adecuado para cada dirección URL. A continuación, el recopilador pasa la dirección URL al controlador de protocolo. El controlador de protocolo tiene acceso al elemento y pasa los metadatos del elemento de vuelta al recopilador. El recopilador utiliza los metadatos para identificar el filtro correcto.

En el diagrama siguiente se muestra una vista de alto nivel del proceso de rastreo de URL. Esta fase incluye una coordinación y una comunicación considerables entre los componentes.

![diagrama que muestra el proceso de rastreo de direcciones URL y acceso a elementos](images/crawlingqueues.jpg)

En el resto de esta sección se describe cómo Windows Search tiene acceso a los elementos para la indexación y explica los roles de cada uno de los componentes implicados.

**Recopilador**  En la fase 2, la fase de rastreo, el recopilador procesa las direcciones URL en las colas, comenzando por la cola de prioridad alta. Cada dirección URL se examina para identificar su Protocolo. A continuación, el recopilador busca el controlador de protocolo registrado para ese protocolo y lo crea en el proceso de búsqueda de host de protocolo.

**Buscar host de protocolo**  El host del Protocolo de búsqueda es simplemente un proceso de host con conversión boxing para los controladores de protocolo. Normalmente, Windows Search crea dos procesos de host, uno que se ejecuta en el contexto de seguridad del sistema y otro que se ejecuta en el contexto de seguridad del usuario. Esta separación garantiza que los datos específicos de un usuario no se ejecuten nunca en el contexto del sistema.

Windows Search también usa el proceso de host para aislar una instancia de un controlador de protocolo de otros procesos o aplicaciones. De este modo, ninguna aplicación externa puede tener acceso a esa instancia específica del controlador de protocolo y, si el controlador de protocolo produce un error inesperadamente, solo se ve afectado el proceso de indización. Dado que el proceso de host ejecuta código de terceros (controladores de protocolo), Windows Search recicla periódicamente el proceso para minimizar el tiempo que un ataque de éxito tiene para aprovechar la información del proceso. Más allá de esto, el host del Protocolo de búsqueda no afecta al rastreo de direcciones URL ni a la indexación de elementos.

**Controladores de protocolo**  Los controladores de protocolo proporcionan acceso a los elementos de un almacén de datos mediante el protocolo del almacén de datos. Por ejemplo, el controlador de protocolo NTFS proporciona acceso a los archivos de una unidad local mediante el protocolo file://. El controlador de protocolo sabe cómo atravesar el almacén de datos, identificar elementos nuevos o actualizados y notificar al recopilador. A continuación, cuando comienza el rastreo, el controlador de protocolo proporciona un objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) al recopilador para enlazar con la secuencia subyacente del elemento y devolver los metadatos del elemento, como las restricciones de seguridad y la hora de la última modificación.

> [!NOTE]  
> Los controladores de Protocolo no son componentes de Windows Search; son componentes del protocolo específico y del almacén de datos a los que están diseñados para tener acceso. Si tiene un almacén de datos personalizado que desea indizar, debe implementar un controlador de protocolo. Para obtener más información sobre los controladores de protocolo y cómo implementar uno, consulte [desarrollar controladores de protocolo](-search-3x-wds-phaddins.md).

**Metadatos y flujo**  Con los metadatos devueltos por el objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del controlador de protocolo, el recopilador identifica el filtro correcto para la dirección URL. El recopilador analiza la extensión de nombre de archivo del elemento y busca el filtro registrado para esa extensión. Si el recopilador no puede encontrar un filtro, Windows Search usa los metadatos para derivar un conjunto mínimo de información de propiedades del sistema (como System. ItemName) y actualiza el índice. De lo contrario, si el recopilador encuentra el filtro, comienza la tercera fase de la indización.

## <a name="stage-3-updating-the-index"></a>Fase 3: actualización del índice

En la tercera fase de la indización, el recopilador crea una instancia del filtro correcto para la dirección URL e inicializa el filtro con la secuencia del objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) . A continuación, el filtro tiene acceso al elemento y devuelve el contenido del índice. Si tiene un formato de archivo personalizado, Windows Search se basa en el filtro para tener acceso a las direcciones URL y emitir el contenido y las propiedades para la indexación.

En el diagrama siguiente se muestra una vista de alto nivel del proceso de acceso a datos. Esta fase incluye una coordinación y una comunicación considerables entre los componentes.

![diagrama que muestra los datos del elemento emitidos para el índice](images/filteringdata.jpg)

En el resto de esta sección se describe cómo Windows Search tiene acceso a los datos de elementos para la indexación y explica los roles de cada uno de los componentes implicados.

**Recopilador**  Al principio de esta fase, el rol del recopilador es crear una instancia del filtro correcto para el elemento y pasarle el flujo del elemento. Al final de esta fase, el recopilador toma el contenido y las propiedades emitidos por el filtro y el controlador de propiedades y actualiza el índice.

**Host de filtro**  El host de filtro es simplemente un proceso de host para los filtros y los controladores de propiedades y sirve para un propósito similar al host del Protocolo de búsqueda. El proceso de host aísla los filtros y los controladores de propiedades del resto del sistema por las mismas razones de seguridad y estabilidad que los procesos de host de protocolo de búsqueda aíslan los controladores de protocolo. El proceso de host se ejecuta con derechos mínimos (no puede tener acceso al sistema de archivos) y se recicla ocasionalmente para protegerse frente a ataques de seguridad. Windows Search también supervisa el uso de recursos para que, si un filtro consume demasiados recursos, se recicle el proceso de host.

**Filtros**  de  Los filtros son componentes críticos en el proceso de indización que emiten información del elemento para el recopilador. Los filtros se denominan después de la interfaz principal utilizada en su implementación, la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y, por consiguiente, se conocen a veces como IFilters. Hay dos tipos de filtros: uno que interactúa con elementos individuales como archivos y otro que interactúa con contenedores como carpetas. Ambos proporcionan datos para el índice.

Con los metadatos devueltos por el objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del controlador de protocolo, el recopilador identifica el filtro correcto para una dirección URL determinada y lo pasa a la secuencia. El recopilador identifica el filtro correcto a través de un controlador de protocolo o de la extensión de nombre de archivo, el tipo MIME o el identificador de clase (CLSID). Si la dirección URL apunta a un contenedor, el filtro emite propiedades para el contenedor y enumera los elementos del contenedor (direcciones URL secundarias). Si la dirección URL apunta a un elemento, el filtro devuelve el contenido textual, si cualquier lectura de las propiedades y es más complejo que los controladores de propiedades. Por lo general, se recomienda que los filtros emitan el contenido de los elementos, mientras que los controladores de propiedades emiten propiedades de elemento. Sin embargo, si el filtro necesita trabajar con aplicaciones antiguas que no reconocen controladores de propiedades, puede implementar el filtro para emitir propiedades también.

> [!NOTE]  
> Los filtros no son componentes de Windows Search; son componentes relacionados con el formato de archivo o contenedor específico al que están diseñados para tener acceso. Para obtener más información sobre los filtros y cómo implementar uno para un contenedor o un formato de archivo personalizado, vea [prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md).

En la tabla siguiente se enumeran los resultados que el recopilador recibe de un filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) y un controlador de propiedades ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante el proceso de indización.

|                            | [**Imaging**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| Permitir escritura                | No                                 | Sí                                             |
| Mezclar contenido y propiedades | Sí                                | No                                              |
| Entornos               | Sí                                | No                                              |
| Emitir vínculos                 | Sí                                | No                                              |
| MIME                       | Sí                                | No                                              |
| Límites de texto            | Oración, párrafo, capítulo       | None                                            |
| Cliente/servidor            | Ambos                               | Remoto                                          |
| Implementación             | Complex                            | Simple                                          |

**Controladores de propiedades**  Los controladores de propiedades son componentes que leen y escriben propiedades para un formato de archivo determinado. Tienen acceso a los elementos y emiten las propiedades del recopilador de la misma manera que los filtros para el contenido. Los controladores de propiedades son más fáciles de implementar que los filtros. Si un formato de archivo basado en texto es muy sencillo o se espera que los archivos sean muy pequeños, el controlador de propiedades puede emitir propiedades y contenido.

> [!NOTE]  
> Los controladores de propiedades no son componentes de Windows Search; son componentes relacionados con el formato de archivo específico al que están diseñados para tener acceso. Para obtener más información sobre los controladores de propiedades y cómo implementar uno para un formato de archivo personalizado, vea [desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Propiedades** de Windows Search proporciona un [sistema de propiedades](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) que incluye una gran biblioteca de propiedades. Cualquier propiedad puede aparecer en cualquier elemento tal y como se define en el filtro o en el controlador de propiedades. Si tiene un formato de archivo personalizado, puede asignar las propiedades del formato de archivo a estas propiedades del sistema, y puede crear nuevas propiedades personalizadas. Cuando el filtro o el controlador de propiedades emite estas propiedades, el recopilador actualiza el índice para que los usuarios puedan buscar con sus propiedades. Para obtener más información sobre cómo crear y registrar propiedades personalizadas para un formato de archivo, vea [sistema de propiedades](../properties/building-property-handlers.md).

**SystemIndex**  El índice, denominado SystemIndex, almacena los datos indexados y se compone de un almacén de propiedades e índices sobre las propiedades y el contenido de las propiedades de los elementos, y un índice invertido para el contenido y las propiedades de texto. Una vez que el recopilador actualiza el índice, la búsqueda de Windows y otras aplicaciones pueden consultar el índice. Para obtener más información sobre las formas de consultar el índice, vea [consultar el índice mediante programación](-search-3x-wds-qryidx-overview.md).

> [!NOTE]  
> Recuerde que, al volver a registrar un esquema, el indizador no respeta los cambios realizados en los atributos de propiedades definidas previamente. La solución consiste en volver a generar el índice o introducir nuevas propiedades que reflejen los cambios en lugar de actualizar los anteriores (no se recomienda). Para obtener más información, vea [Nota para los implementadores](#notes-to-implementers) en [propiedades información general del sistema](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Cómo se programa la indexación

Cuando Windows Search se instala por primera vez, realiza una indexación completa del ámbito de rastreo, en pausa durante períodos de gran actividad de e/s y del usuario. El ámbito de rastreo predeterminado consta de las ubicaciones predeterminadas de la biblioteca, como **documentos**, **música**, **imágenes** y **vídeos**. Las notificaciones se procesan incluso antes de que finalice el rastreo inicial. En ocasiones, el recopilador rastrea las direcciones URL del ámbito de rastreo completo. Estos rastreos completos garantizan que los datos del índice estén actualizados. Por ejemplo, si un proveedor de notificaciones no puede enviar notificaciones o si el servicio de Windows Search finaliza de forma inesperada, el recopilador no tendrá ningún conocimiento de los elementos nuevos o modificados y no indizará estos elementos. Hay dos tipos de orígenes: solo notificación y notificación habilitada. En ambos orígenes, el recopilador rastrea inicialmente el índice. Después del rastreo inicial, los orígenes de solo notificación nunca realizarán un rastreo completo de nuevo a menos que se produzca un error, como el [diario de cambios de USN](/windows/desktop/FileIO/change-journals) que se revierte. Los orígenes habilitados para notificaciones realizan un rastreo incremental cuando se inicia el indexador, pero después escuchan las notificaciones mientras se ejecutan. NTFS y Microsoft Outlook son solo notificaciones. Internet Explorer y FAT están habilitadas para notificaciones.

## <a name="notes-to-implementers"></a>Notas a los implementadores

La calidad de los datos en el índice y la eficacia del proceso de indexación dependen en gran medida de la implementación del controlador de propiedades y el filtro. Dado que se llama al filtro cada vez que una dirección URL identifica el formato de archivo, el proceso de indexación puede reducirse drásticamente si el filtro es ineficaz. Si el controlador de propiedad no asigna correctamente todas las propiedades de archivo a las propiedades del sistema o no emite correctamente estas propiedades, los datos del índice serán incorrectos y las búsquedas posteriores de esas propiedades devolverán resultados incorrectos. Si se produce un error en el controlador de filtro o propiedad, el indexador no podrá indizar los datos.

Las aplicaciones y los procesos distintos de Windows Search se basan en los controladores de protocolo, filtros y controladores de propiedades. Las implementaciones pueden afectar a las aplicaciones de la manera que pueda no esperar. La [Guía de desarrollo de Windows Search](-search-developers-guide-entry-page.md) proporciona consejos sobre las opciones de diseño y la prueba de cada uno de estos componentes.

## <a name="related-topics"></a>Temas relacionados

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)

[Qué se incluye en el índice](-search-indexing-process-overview.md)

[Consulta del proceso en Windows Search](querying-process--windows-search-.md)

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
