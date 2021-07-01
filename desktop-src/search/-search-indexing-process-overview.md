---
description: En este tema se describen las tres fases del proceso de indexación y los componentes principales implicados en cada una, se explica el tiempo de la actividad de indexación y se proporcionan algunas notas para desarrolladores de terceros que desean indexar sus almacenes de datos o formatos de archivo.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Proceso de indexación en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b819a056b9a3dd44ea799ee56ae6b2e87606f552
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119540"
---
# <a name="indexing-process-in-windows-search"></a>Proceso de indexación en Windows Search

En este tema se describen las tres fases del proceso de indexación y los componentes principales implicados en cada una, se explica el tiempo de la actividad de indexación y se proporcionan algunas notas para desarrolladores de terceros que desean indexar sus almacenes de datos o formatos de archivo.

Este tema se organiza de la siguiente manera:

- [Información general](#overview)
- [Fase 1: Puesta en cola de direcciones URL para indexación](#stage-1-queuing-urls-for-indexing)
- [Fase 2: Rastreo de direcciones URL](#stage-2-crawling-urls)
- [Fase 3: Actualización del índice](#stage-3-updating-the-index)
- [Cómo se programa la indexación](#how-indexing-is-scheduled)
- [Notas a los implementadores](#notes-to-implementers)
- [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Windows Search admite la indexación de propiedades y contenido de archivos de diferentes formatos de archivo, como formatos .doc o .jpeg, y almacenes de datos, como el sistema de archivos o los buzones de Windows Outlook. Hay dos tipos de índices: índices de valor que permiten filtrar y ordenar por el valor completo de una propiedad e índices invertidos que indexan palabras dentro de propiedades textuales o contenido. Si tiene un almacén de datos o un formato de archivo personalizado, debe comprender cómo Windows Search índices para que los elementos se indexe correctamente.

El proceso de indexación se produce en tres fases controladas por un Windows Search denominado recopilador. En la primera fase, el recopilador agrega direcciones URL a las colas. Las direcciones URL identifican los elementos que se van a indexar y las colas son simplemente listas de direcciones URL con prioridad. En la segunda fase, el recopilador coordina otros componentes Windows Search y de terceros para acceder a los elementos y recopilar datos sobre ellos. Por último, en la tercera fase, los datos recopilados se agregan al índice.

En el diagrama siguiente se muestran los componentes principales y el flujo de datos a través del proceso de indexación. Varios componentes participan en la recopilación de datos para el índice. Algunas de ellas forman parte de Windows Search y otras proceden de aplicaciones de terceros. Si tiene un almacén de datos personalizado o un formato de archivo, Windows Search se basa en el controlador de protocolo y filtra para acceder a las direcciones URL y emitir propiedades para la indexación. Windows Search componentes se muestran en azul y los componentes de terceros se muestran en verde.

![diagrama que muestra la interacción entre los componentes durante el proceso de indexación](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Fase 1: Puesta en cola de direcciones URL para indexación

En la primera fase de la indexación, el recopilador recopila información sobre las actualizaciones de los almacenes de datos, la compara con el ámbito de rastreo conocido y, a continuación, crea una cola de direcciones URL para recorrer para recopilar datos para el índice. En el caso de los orígenes que no se basan en la notificación, como las unidades FAT, el recopilador inicia periódicamente un recorrido completo del ámbito de rastreo para que los datos del índice se mantienen nuevos. Para orígenes como NTFS, solo hay un rastreo y todo lo demás se controla mediante notificaciones del diario de [cambios de USN](/windows/desktop/FileIO/change-journals). Tampoco hay ningún rastreo de Microsoft Outlook. En el diagrama siguiente se muestra una vista general del proceso de cola para la indexación sin rastreo.

![diagrama que muestra el proceso de consulta para la indexación sin rastreo](images/queuingurls.jpg)

En el resto de esta sección se explica cómo Windows Search las direcciones URL que se rastrearán y se definen algunos términos importantes a lo largo del proceso.

**Ámbito de rastreo**  El ámbito de rastreo es un conjunto de direcciones URL que Windows Search para recopilar datos sobre elementos que el usuario quiere indexar para búsquedas más rápidas. Windows Search agrega algunas direcciones URL al ámbito de rastreo de forma predeterminada, como las rutas de acceso a las carpetas **Documentos** **e Imágenes de los** usuarios. Otras direcciones URL se pueden agregar mediante aplicaciones, usuarios y directiva de grupo. Por último, tanto los usuarios directiva de grupo pueden excluir explícitamente las direcciones URL. Windows Search todas las direcciones URL agregadas y quita las direcciones URL excluidas para determinar el ámbito de rastreo. Este es el conjunto de trabajo de direcciones URL desde las que el recopilador comienza su trabajo.

**Recopilador**  El recopilador es un Windows Search que recopila información sobre las direcciones URL dentro del ámbito de rastreo y crea una cola de direcciones URL para que el indexador lo rastree. Cuando se agrega, elimina o actualiza un elemento del ámbito de rastreo, el proveedor de notificaciones del almacén de datos notifica al recopilador. Hay un rastreo inicial en el que el recopilador comienza en la raíz del ámbito de rastreo. La dirección URL se pasa al controlador de protocolo y, a continuación, al [**IFilter adecuado.**](/windows/win32/api/filter/nn-filter-ifilter) El filtro suele ser una enumeración de directorio que genera más direcciones URL. Las notificaciones son el estado estable. Normalmente, cada almacén de datos tiene su propio controlador de protocolo que proporciona estas notificaciones. Por ejemplo, en el sistema de archivos local, el diario de cambios [de USN](/windows/desktop/FileIO/change-journals) actúa como proveedor de notificaciones para todas las direcciones URL del protocolo file:// datos. De forma similar, Microsoft Outlook actúa como proveedor de notificaciones para todas las direcciones URL del mapi:// protocolo. Cuando un usuario recibe, mueve o elimina correo electrónico, Outlook notifica al recopilador el estado modificado del correo electrónico. A partir de estas notificaciones, el recopilador crea colas de indexación de direcciones URL para rastrear.

**Indexación de colas**  Las colas de indexación son listas de direcciones URL que identifican los elementos que se deben indexar o volver a indexar. El recopilador compara las direcciones URL que recibe de los proveedores de notificaciones con las direcciones URL del ámbito de rastreo. Todas las direcciones URL de los proveedores de notificaciones que se encuentran dentro del ámbito de rastreo se agregan a una cola que el recopilador usa para priorizar las direcciones URL que se van a procesar a continuación.

Hay tres colas: notificaciones de prioridad alta, notificaciones normales y rastreos periódicos. La cola de prioridad alta es para las notificaciones que se deben procesar inmediatamente. Por ejemplo, cuando un usuario cambia la propiedad title de un elemento en Explorador de Windows, la vista Explorador de Windows debe actualizarse inmediatamente después del cambio. La cola de notificaciones normal es para todas las notificaciones de cambio restantes. Las colas de notificación se procesan antes que la cola de rastreo porque es más probable que los elementos modificados sean de interés para un usuario. El recopilador accede a los datos de las direcciones URL de cada cola en orden primero en entrada y salida (FIFO).

Para obtener más información sobre la priorización y las API de eventos introducidas en Windows 7, vea [Indexing Prioritization and Rowset Events in Windows 7](indexing-prioritization-and-rowset-events.md). Para obtener más información sobre la administración del ámbito de rastreo y las notificaciones, vea Proporcionar notificaciones [de cambios](-search-3x-wds-notifyingofchanges.md) y Usar [el Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Fase 2: Rastreo de direcciones URL

En la segunda fase de la indexación, el recopilador rastrea las colas, accede a los almacenes de datos y recupera secuencias de elementos. En primer lugar, el recopilador busca el controlador de protocolo adecuado para cada dirección URL. A continuación, el recopilador pasa la dirección URL al controlador de protocolo. El controlador de protocolo tiene acceso al elemento y pasa los metadatos del elemento al recopilador. El recopilador usa los metadatos para identificar el filtro correcto.

En el diagrama siguiente se muestra una vista general del proceso de rastreo de direcciones URL. Esta fase incluye una coordinación y comunicación considerables entre los componentes.

![diagrama que muestra el proceso de rastreo de direcciones URL y acceso a elementos](images/crawlingqueues.jpg)

En el resto de esta sección se describe Windows Search acceso a elementos para la indexación y se explican los roles de cada uno de los componentes implicados.

**Recopilador**  En la fase 2, la fase de rastreo, el recopilador procesa las direcciones URL de las colas, empezando por la cola de prioridad alta. Cada dirección URL se examina para identificar su protocolo. A continuación, el recopilador busca el controlador de protocolo registrado para ese protocolo y lo crea una instancia en el proceso de host del protocolo de búsqueda.

**Host de protocolo de búsqueda**  El host de protocolo de búsqueda es simplemente un proceso de host con conversión boxed para los controladores de protocolo. Normalmente, Windows Search dos procesos host de este tipo, uno que se ejecuta en el contexto de seguridad del sistema y otro que se ejecuta en el contexto de seguridad del usuario. Esta separación garantiza que los datos específicos de un usuario nunca se ejecuten en el contexto del sistema.

Windows Search también usa el proceso de host para aislar una instancia de un controlador de protocolo de otros procesos o aplicaciones. De este modo, ninguna aplicación externa puede acceder a esa instancia específica del controlador de protocolo y, si se produce un error inesperado en el controlador de protocolo, solo se ve afectado el proceso de indexación. Dado que el proceso host ejecuta código de terceros (controladores de protocolo), Windows Search recicla periódicamente el proceso para minimizar el tiempo que un ataque correcto tiene para aprovechar la información del proceso. Más allá de esto, el host del protocolo de búsqueda no afecta al rastreo de direcciones URL ni a la indexación de elementos.

**Controladores de protocolo**  Los controladores de protocolo proporcionan acceso a los elementos de un almacén de datos mediante el protocolo del almacén de datos. Por ejemplo, el controlador de protocolo NTFS proporciona acceso a los archivos de una unidad local mediante file:// protocolo. El controlador de protocolos sabe cómo atravesar el almacén de datos, identificar elementos nuevos o actualizados y notificar al recopilador. A continuación, cuando comienza el rastreo, el controlador de protocolo proporciona un objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) al recopilador para enlazarse a la secuencia subyacente del elemento y devolver metadatos de elemento como restricciones de seguridad y la hora de la última modificación.

> [!NOTE]  
> Los controladores de protocolo no Windows Search componentes; son componentes del protocolo y almacén de datos específicos a los que están diseñados para acceder. Si tiene un almacén de datos personalizado que desea indexar, debe implementar un controlador de protocolo. Para obtener más información sobre los controladores de protocolo y cómo implementar uno, consulte [Desarrollo de controladores de protocolo.](-search-3x-wds-phaddins.md)

**Metadatos y secuencia**  Con los metadatos devueltos por el objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del controlador de protocolo, el recopilador identifica el filtro correcto para la dirección URL. El recopilador analiza la extensión de nombre de archivo del elemento y busca el filtro registrado para esa extensión. Si el recopilador no encuentra un filtro, Windows Search usa los metadatos para derivar un conjunto mínimo de información de propiedades del sistema (como System.ItemName) y actualiza el índice. De lo contrario, si el recopilador encuentra el filtro, comienza la tercera fase de indexación.

## <a name="stage-3-updating-the-index"></a>Fase 3: Actualización del índice

En la tercera fase de indexación, el recopilador crea una instancia del filtro correcto para la dirección URL e inicializa el filtro con la secuencia del objeto [**IUrlAccessor.**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) A continuación, el filtro accede al elemento y devuelve el contenido del índice. Si tiene un formato de archivo personalizado, Windows Search se basa en el filtro para acceder a las direcciones URL y emitir contenido y propiedades para la indexación.

En el diagrama siguiente se muestra una vista general del proceso de acceso a datos. Esta fase incluye una coordinación y comunicación considerables entre los componentes.

![diagrama que muestra los datos de elementos emitidos para el índice](images/filteringdata.jpg)

En el resto de esta sección se describe Windows Search acceso a los datos de elementos para la indexación y se explican los roles de cada uno de los componentes implicados.

**Recopilador**  Al principio de esta fase, el rol del recopilador es crear una instancia del filtro correcto para el elemento y pasarlo a la secuencia de elementos. Al final de esta fase, el recopilador toma el contenido y las propiedades emitidos por el controlador de filtro y propiedad y actualiza el índice.

**Host de filtro**  El host de filtro es simplemente un proceso de host para filtros y controladores de propiedades y tiene un propósito similar al host del protocolo de búsqueda. El proceso de host aísla los filtros y los controladores de propiedades del resto del sistema por las mismas razones de seguridad y estabilidad que los procesos de host de protocolo de búsqueda aíslan los controladores de protocolo. El proceso de host se ejecuta con derechos mínimos (ni siquiera puede acceder al sistema de archivos) y, en ocasiones, se recicla para protegerse frente a ataques de seguridad. Windows Search también supervisa el uso de recursos para que si un filtro consume demasiados recursos, se recicla el proceso de host.

**Filtros**  Los filtros son componentes críticos del proceso de indexación que emiten información de elementos para el recopilador. Los filtros se denominan después de la interfaz principal usada en su implementación, la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y, por tanto, a veces se conocen como IFilters. Hay dos tipos de filtros: uno que interactúa con elementos individuales como archivos y otro que interactúa con contenedores como carpetas. Ambos proporcionan datos para el índice.

Con los metadatos devueltos por el objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del controlador de protocolo, el recopilador identifica el filtro correcto para una dirección URL determinada y lo pasa a la secuencia. El recopilador identifica el filtro correcto a través de un controlador de protocolo o mediante la extensión de nombre de archivo, el tipo MIME o el identificador de clase (CLSID). Si la dirección URL apunta a un contenedor, el filtro emite propiedades para el contenedor y enumera los elementos del contenedor (direcciones URL secundarias). Si la dirección URL apunta a un elemento, el filtro devuelve el contenido textual, si hay alguna lectura de propiedades y es más complejo que los controladores de propiedades. Por lo general, se recomienda que los filtros emitan contenido del elemento mientras que los controladores de propiedades emiten propiedades de elemento. Sin embargo, si el filtro necesita trabajar con aplicaciones anteriores que no reconocen controladores de propiedades, también puede implementar el filtro para emitir propiedades.

> [!NOTE]  
> Los filtros no son Windows Search componentes; son componentes relacionados con el formato de archivo o contenedor específico al que están diseñados para acceder. Para obtener más información sobre los filtros y cómo implementar uno para un contenedor o formato de archivo personalizado, vea [Procedimientos recomendados](-search-3x-wds-extidx-filters.md)para crear controladores de filtro en Windows Search .

En la tabla siguiente se enumeran los resultados que recibe el recopilador de un filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) y el controlador de propiedades ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante el proceso de indexación.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Permitir escritura**                | No                                 | Sí                                             |
| **Combinación de contenido y propiedades** | Sí                                | No                                              |
| **Multilingüe**               | Sí                                | No                                              |
| **Emisión de vínculos**                 | Sí                                | No                                              |
| **Mime**                       | Sí                                | No                                              |
| **Límites de texto**            | Oración, párrafo, capítulo       | Ninguno                                            |
| **Cliente o servidor**            | Ambos                               | Cliente                                          |
| **Implementación**             | Complex                            | Simple                                          |

**Controladores de propiedades**  Los controladores de propiedades son componentes que leen y escriben propiedades para un formato de archivo determinado. Acceden a los elementos y emiten propiedades para el recopilador de la misma manera que los filtros para el contenido. Los controladores de propiedades son más fáciles de implementar que los filtros. Si un formato de archivo basado en texto es muy sencillo o se espera que los archivos sean muy pequeños, el controlador de propiedades puede emitir propiedades y contenido.

> [!NOTE]  
> Los controladores de propiedades no Windows Search componentes; son componentes relacionados con el formato de archivo específico al que están diseñados para acceder. Para obtener más información sobre los controladores de propiedades y cómo implementar uno para un formato de archivo personalizado, vea [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Propiedades** Windows Search proporciona un [sistema de propiedades](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) que incluye una gran biblioteca de propiedades. Cualquier propiedad puede aparecer en cualquier elemento tal como se define en el filtro o controlador de propiedades. Si tiene un formato de archivo personalizado, puede asignar las propiedades del formato de archivo a estas propiedades del sistema y puede crear nuevas propiedades personalizadas. Cuando el controlador de propiedades o filtros emite estas propiedades, el recopilador actualiza el índice para que los usuarios puedan buscar con sus propiedades. Para obtener más información sobre cómo crear y registrar propiedades personalizadas para un formato de archivo, vea [Property System](../properties/building-property-handlers.md).

**SystemIndex**  El índice, denominado SystemIndex, almacena datos indexados y se compone de un almacén de propiedades e índices sobre las propiedades y el contenido de las propiedades de los elementos, y un índice invertido para el contenido textual y las propiedades. Una vez que el recopilador actualiza el índice, el índice se puede consultar Windows Search otras aplicaciones. Para obtener más información sobre las formas de consultar el índice, vea [Consultar el índice mediante programación.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Recuerde que al volver a registrar un esquema, es posible que el indexador no respete los cambios realizados en los atributos de las propiedades definidas previamente. La solución es recompilar el índice o introducir nuevas propiedades que reflejen los cambios en lugar de actualizar los antiguos (no recomendado). Para obtener más información, vea [Note to Implementers](#notes-to-implementers) in [Properties System Overview](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Cómo se programa la indexación

Cuando Windows Search se instala por primera vez, realiza una indexación completa del ámbito de rastreo, pausando durante períodos de E/S alta y actividad del usuario. El ámbito de rastreo predeterminado consta de las ubicaciones de biblioteca predeterminadas, como **Documentos,** **Música,** **Imágenes** y **Vídeos.** Las notificaciones se procesan incluso antes de que finalice el rastreo inicial. En ocasiones, el recopilador rastrea las direcciones URL del ámbito de rastreo completo. Estos rastreos completos garantizan que los datos del índice están nuevos. Por ejemplo, si un proveedor de notificaciones no puede enviar notificaciones o si el servicio de Windows Search finaliza inesperadamente, el recopilador no tendría conocimiento de los elementos nuevos o modificados y no los indexaría. Hay dos tipos de orígenes: solo notificación y notificación habilitada. En ambos orígenes, el recopilador rastrea inicialmente el índice. Después del rastreo inicial, los orígenes de solo notificación nunca volverán a realizar un rastreo completo a menos que se produce un error, como la suminación de [USN Change Journal.](/windows/desktop/FileIO/change-journals) Los orígenes habilitados para notificaciones hacen un rastreo incremental cuando se inicia el indexador, pero luego escuchan las notificaciones mientras se ejecutan. NTFS y Microsoft Outlook son solo notificaciones. Internet Explorer y FAT son notificaciones habilitadas.

## <a name="notes-to-implementers"></a>Notas a los implementadores

La calidad de los datos del índice y la eficacia del proceso de indexación dependen en gran medida de la implementación del controlador de propiedades y filtros. Dado que se llama al filtro cada vez que una dirección URL identifica el formato de archivo, el proceso de indexación puede ralentizarse considerablemente si el filtro es ineficaz. Si el controlador de propiedades no asigna correctamente todas las propiedades de archivo a las propiedades del sistema o no emite correctamente estas propiedades, los datos del índice serán incorrectos y las búsquedas posteriores de esas propiedades devolverán resultados incorrectos. Si se produce un error en el controlador de filtro o propiedad, el indexador no podrá indexar los datos.

Las aplicaciones y los procesos que no Windows Search se basan en controladores de protocolo, filtros y controladores de propiedades. Las implementaciones pueden afectar a esas aplicaciones de maneras que no se esperen. La [guía Windows Search desarrollo proporciona](-search-developers-guide-entry-page.md) consejos sobre las opciones de diseño y sobre la prueba de cada uno de estos componentes.

## <a name="related-topics"></a>Temas relacionados

[Indexación, consulta y notificaciones en Windows Search](-search-3x-wds-included-in-index.md)

[Qué se incluye en el índice](-search-indexing-process-overview.md)

[Proceso de consulta en Windows Search](querying-process--windows-search-.md)

[Proceso de notificaciones en Windows Search](-search-3x-wds-support.md)

[Requisitos de formato de dirección URL](url-formatting-requirements.md)
