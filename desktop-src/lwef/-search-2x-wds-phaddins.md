---
title: Desarrollo de complementos de controlador de protocolos
description: Puede extender Microsoft Windows Desktop Search (WDS) para incluir nuevos almacenes de datos implementando un controlador de protocolo personalizado.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726505"
---
# <a name="developing-protocol-handler-add-ins"></a>Desarrollo de complementos de controlador de protocolos

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Puede extender Microsoft Windows Desktop Search (WDS) para incluir nuevos almacenes de datos implementando un controlador de protocolo personalizado.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexación de almacenes de datos con controladores de protocolo

Un almacén de datos es un origen de contenido (un sistema de base de datos, un directorio, un sistema de archivos) donde se almacenan los datos y se pueden rastrear mediante el indexador WDS. El almacén puede ser jerárquico (como una base de datos) o basado en vínculos (como un sitio web). Un controlador de protocolo permite que aplicaciones de indexación como WDS rastreen sistemáticamente los nodos de un almacén de datos para extraer información pertinente para incluirla en el índice. Cada controlador de protocolo se usa para indexar un tipo específico de almacén de datos. WDS incluye controladores de protocolo para almacenes del sistema de archivos y para almacenes de datos de Microsoft Outlook y Microsoft Outlook Express (almacenes de correo electrónico, . Archivos PST, y así sucesivamente). Al indexar Outlook correo electrónico, por ejemplo, el controlador de protocolo rastrea todos los mensajes de todas las carpetas que extraen información de cada mensaje y datos adjuntos. Esta información se pasa al indexador para incluirla en el catálogo de WDS.

A menudo, los usuarios necesitan buscar en otros almacenes de datos, como bases de datos heredadas, almacenes de correo electrónico o estructuras de datos no compatibles con WDS. Puede extender WDS para rastrear un nuevo almacén de datos mediante o implementando un controlador de protocolo específicamente para ese almacén de datos. En primer lugar, primero debe determinar si ya existe un controlador de protocolo para el almacén de datos, quizás para su uso con otra aplicación como SharePoint Services. Si es así, puede instalar ese controlador de protocolo en el sistema. Sin embargo, si no existe otro controlador de protocolo, deberá implementar uno. Los controladores de protocolo WDS usan las mismas especificaciones de diseño que SharePoint Services, y a menudo se pueden usar indistintamente.

Además, si el almacén de datos contiene tipos de datos o archivos distintos de uno de los 200 tipos de archivo admitidos por WDS, también debe implementar un filtro para tener acceso e indexar el contenido de los elementos del almacén. WDS 2.x usa el controlador de protocolos y la [**tecnología IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que usa SharePoint Services. Si ya tiene filtros para un almacén y un tipo de archivo específicos instalados en el sistema que se va a indexar, WDS usa las interfaces existentes para indexar estos datos.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Hoja de ruta para agregar nuevos almacenes de datos

Para extender WDS para rastrear nuevos almacenes de datos, puede crear un controlador de protocolo y uno o varios de los siguientes complementos: controlador de menú contextual, controlador de iconos y un complemento SearchProtocolOptions.

1.  Cree y registre un controlador de protocolo multiproceso para el almacén de datos:
    -   **ISearchProtocol:** esta interfaz accede a un protocolo y asigna una dirección URL a un IUrlAccessor.
    -   **IUrlAccessor:** esta es la interfaz principal que se usa para acceder a elementos desde el origen de contenido y enlazar el contenido al filtro adecuado.
    -   **IProtocolHandlerSite:** esta interfaz se usa para solicitar y cargar filtros adicionales.
    -   **IFilter:** esta interfaz devuelve la dirección URL de cada elemento de una carpeta como propiedades de valor para el procesamiento.

    > [!Note]
    >
    > La funcionalidad mínima de complemento necesaria para devolver los resultados de búsqueda de un almacén de datos no jerárquico es una implementación de las interfaces ISearchProtocol e IUrlAccessor.

     

2.  Implemente la interfaz ISearchProtocolOptions para incluir opciones de controlador de protocolo personalizadas, como páginas de inicio predefinidas:
    -   **ISearchProtocolOptions:** esta interfaz define las direcciones URL predeterminadas que debe procesar el controlador de protocolos, determina cuáles son los requisitos de un controlador de protocolo y determina si se han cumplido los requisitos en un sistema determinado.
3.  Amplíe Shell para incluir elementos de la interfaz de usuario, como menús contextuales e iconos específicos del archivo, mediante la implementación de las interfaces siguientes:
    -   **IShellFolder:** esta interfaz, que se usa para administrar carpetas, es necesaria para proporcionar las interfaces IContextMenu e IExtractIcon para una dirección URL en un nuevo almacén.
    -   **IPersistFolder: esta** interfaz es necesaria para indicar a un objeto de carpeta de Shell que se inicialice.
    -   **IPersist:** esta interfaz proporciona el identificador de clase (CLSID) de un objeto que se puede almacenar de forma persistente en el sistema.
    -   **IContextMenu:** esta interfaz define el menú contextual con el botón derecho para un elemento al que apunta la dirección URL.
    -   **IExtractIcon:** esta interfaz define el icono que se va a mostrar para un elemento al que apunta la dirección URL.
4.  Implemente un mecanismo para notificar al indexador los cambios en el almacén de datos:
    -   **ISearchItemsChangedSink:** esta interfaz permite que el controlador de protocolo notifique al índice los cambios en el almacén de datos. Esto mejora el rendimiento al garantizar que el indexador no rastree todo el almacén en índices incrementales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Implementar un controlador de protocolo para WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Agregar iconos, vistas previas y menús contextuales con extensiones de shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notificación al índice de cambios](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 