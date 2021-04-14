---
title: Desarrollar complementos de controlador de protocolo
description: Puede extender la búsqueda de escritorio de Microsoft Windows (WDS) para incluir nuevos almacenes de datos mediante la implementación de un controlador de protocolo personalizado.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a8688621f7d2fda653d769c0e1dfdadd240f49
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533172"
---
# <a name="developing-protocol-handler-add-ins"></a>Desarrollar complementos de controlador de protocolo

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Puede extender la búsqueda de escritorio de Microsoft Windows (WDS) para incluir nuevos almacenes de datos mediante la implementación de un controlador de protocolo personalizado.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexación de almacenes de datos con controladores de protocolo

Un almacén de datos es un origen de contenido (un sistema de base de datos, un directorio, un sistema de archivos) en el que se almacenan los datos y se pueden rastrear mediante el indexador de WDS. El almacén puede ser jerárquico (como una base de datos) o basado en vínculo (como un sitio web). Un controlador de protocolo permite que las aplicaciones de indización como WDS rastreen sistemáticamente los nodos de un almacén de datos para extraer información relevante que se incluirá en el índice. Cada controlador de protocolo se utiliza para indizar un tipo específico de almacén de datos. WDS se suministra con los controladores de protocolo para los almacenes del sistema de archivos y para los almacenes de datos de Microsoft Outlook y Microsoft Outlook Express (almacenes de correo electrónico,. Archivos PST, etc.). Al indizar el correo electrónico de Outlook, por ejemplo, el controlador de protocolo rastrea todos los mensajes de todas las carpetas extrayendo información de cada mensaje y datos adjuntos. Esta información se pasa al indizador que se va a incluir en el catálogo de WDS.

A menudo, los usuarios necesitan buscar otros almacenes de datos, como bases de datos heredadas, almacenes de correo electrónico o estructuras de datos no admitidas por WDS. Puede extender WDS para rastrear un nuevo almacén de datos mediante o implementando un controlador de protocolo específicamente para ese almacén de datos. En primer lugar, debe determinar primero si ya existe un controlador de protocolo para el almacén de datos, quizás para su uso con otra aplicación como SharePoint Services. Si es así, puede instalar el controlador de protocolo en el sistema. Sin embargo, si no existe otro controlador de protocolo, debe implementar uno. Los controladores de protocolo de WDS usan las mismas especificaciones de diseño que SharePoint Services y, a menudo, se pueden usar indistintamente.

Además, si el almacén de datos contiene datos o tipos de archivo distintos de uno de los tipos de archivo 200 que admite WDS, también debe implementar un filtro para obtener acceso al contenido de los elementos del almacén e indexarlo. WDS 2. x usa el controlador de protocolo y la tecnología de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)usada por SharePoint Services. Si ya tiene filtros para un almacén específico y un tipo de archivo instalados en el sistema que se está indizando, WDS usa las interfaces existentes para indizar estos datos.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Guía básica para agregar nuevos almacenes de datos

Para ampliar WDS para que rastree nuevos almacenes de datos, puede crear un controlador de protocolo y uno o varios de los siguientes complementos: controlador de menú contextual, controlador de iconos y un complemento SearchProtocolOptions.

1.  Cree y registre un controlador de protocolo multiproceso para el almacén de datos:
    -   **ISearchProtocol** : esta interfaz tiene acceso a un protocolo y asigna una dirección URL a un IUrlAccessor.
    -   **IUrlAccessor** : esta es la interfaz principal que se usa para obtener acceso a los elementos del origen de contenido y enlazar el contenido con el filtro adecuado.
    -   **IProtocolHandlerSite** : esta interfaz se usa para solicitar y cargar filtros adicionales.
    -   **IFilter** : esta interfaz devuelve la dirección URL de cada elemento de una carpeta como propiedades de valor para el procesamiento.

    > [!Note]
    >
    > La funcionalidad de complementos mínima necesaria para devolver los resultados de la búsqueda desde un almacén de datos no jerárquico es una implementación de las interfaces ISearchProtocol e IUrlAccessor.

     

2.  Implemente la interfaz ISearchProtocolOptions para incluir opciones de controlador de protocolo personalizadas, como páginas de inicio predefinidas:
    -   **ISearchProtocolOptions** : esta interfaz define las direcciones URL predeterminadas que el controlador de protocolo debe procesar, determina cuáles son los requisitos de un controlador de protocolo y determina si se han cumplido los requisitos en un sistema determinado.
3.  Extienda el shell para incluir los elementos de la interfaz de usuario, como los menús contextuales y los iconos específicos del archivo, mediante la implementación de las interfaces siguientes:
    -   **IShellFolder** : esta interfaz, que se usa para administrar carpetas, es necesaria para proporcionar las interfaces IContextMenu e IExtractIcon para una dirección URL en un nuevo almacén.
    -   **IPersistFolder** : esta interfaz es necesaria para indicar a un objeto de la carpeta de Shell que se inicialice a sí mismo.
    -   **IPersist** : esta interfaz proporciona el identificador de clase (CLSID) de un objeto que se puede almacenar de forma persistente en el sistema.
    -   **IContextMenu** : esta interfaz define el menú contextual del clic con el botón secundario para un elemento señalado por la dirección URL.
    -   **IExtractIcon** : esta interfaz define el icono que se va a mostrar para un elemento señalado por la dirección URL.
4.  Implemente un mecanismo para notificar a los cambios del indexador en el almacén de datos:
    -   **ISearchItemsChangedSink** : esta interfaz permite al controlador de protocolo notificar al índice de cambios en el almacén de datos. Esto mejora el rendimiento, ya que garantiza que el indexador no rastrea todo el almacén en los índices incrementales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Implementar un controlador de protocolo para WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Agregar iconos, vistas previas y menús contextuales con extensiones de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notificar el índice de cambios](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 