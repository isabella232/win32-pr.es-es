---
description: Algunas aplicaciones almacenan sus elementos en bases de datos o tipos de archivo personalizados.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Descripción de los controladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705500"
---
# <a name="understanding-protocol-handlers"></a>Descripción de los controladores de protocolo

Algunas aplicaciones almacenan sus elementos en bases de datos o tipos de archivo personalizados. Aunque Windows Search puede indizar el nombre y las propiedades del archivo, Windows no tiene ningún conocimiento del contenido del archivo. Como resultado, estos elementos no se pueden indizar ni exponer en el shell de Windows. Al crear un controlador de protocolo, puede hacer que estos elementos estén disponibles para la indexación. También puede indexar un formato de archivo compuesto como un archivo. zip.

Este tema se organiza de la siguiente manera:

-   [Indexación de almacenes de datos con controladores de protocolo](#indexing-data-stores-with-protocol-handlers)
    -   [Almacenes de datos de Shell](#shell-data-stores)
    -   [Controladores de protocolo](#protocol-handlers)
    -   [Filtros y controladores de protocolo](#filters-and-protocol-handlers)
-   [Indexación de un formato de archivo compuesto](#indexing-a-compound-file-format)
-   [Temas relacionados](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexación de almacenes de datos con controladores de protocolo

Cuando los usuarios necesitan buscar bases de datos heredadas, almacenes de correo electrónico u otras estructuras de datos que no son compatibles con Windows Search, debe determinar primero si ya existe un controlador de protocolo para ese almacén de datos, quizás para su uso con otra aplicación como SharePoint Server. Si es así, puede instalar el controlador de protocolo en el sistema. Los controladores de protocolo de Windows Search usan especificaciones de diseño similares a las de SharePoint Server y, a menudo, se pueden usar indistintamente.

Para obtener más información acerca de la implementación de Search Server 2008 con Office SharePoint Server 2007, consulte servidor de búsqueda de búsqueda [federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Almacenes de datos de Shell

Antes de que un desarrollador de terceros con nuevos formatos de archivo y almacenes de datos pueda obtener esos formatos y almacenes para que aparezcan en los resultados de la consulta en el explorador de Windows, el desarrollador debe implementar un origen de datos de Shell. Un origen de datos de Shell es un componente que se utiliza para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos. Un almacén de datos es un repositorio de datos. Un almacén de datos se puede exponer en el modelo de programación de shell como un contenedor que usa un origen de datos de Shell. El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo. El controlador de protocolo implementa el protocolo para tener acceso a un origen de contenido en su formato nativo. Las interfaces [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) y [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) se usan para implementar un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indizar.

Si desea que los resultados de la consulta aparezcan en el explorador de Windows, debe implementar un origen de datos de Shell antes de poder crear un controlador de protocolo para extender el índice. Sin embargo, si todas las consultas se realizarán mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, no es estrictamente necesario un espacio de nombres de Shell que se prefiera todavía.

> [!Note]  
> Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. Un controlador a veces se conoce como una extensión de shell o un controlador de extensión de Shell.

 

Si desea que los usuarios vean los resultados de la búsqueda desde el explorador de Windows, debe crear un controlador de protocolo y uno o varios de los siguientes complementos:

-   Controlador del menú contextual
-   Controlador de iconos
-   Otro tipo de controlador de archivos

Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando conseguir, vea "información general de los controladores" en [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md). Para obtener información sobre cómo crear controladores, vea [registrar extensiones de Shell](../shell/reg-shell-exts.md), [menú contextual](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))y [controladores de tipo de archivo](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Controladores de protocolo

Si el almacén de datos también es un contenedor (por ejemplo, una carpeta del sistema de archivos), debe implementar un filtro para enumerar las direcciones URL del contenedor. Si el almacén de datos contiene datos o tipos de archivo distintos de uno de los tipos de archivo 200 que admite Windows Search, debe implementar un filtro para obtener acceso al contenido de los elementos del almacén e indexarlo. Windows Search usa el controlador de protocolo y la tecnología de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) similar a la usada por SharePoint Server. Si ya tiene filtros para un almacén específico y un tipo de archivo instalados en el sistema que se está indizando, es posible que Windows Search pueda usar las interfaces existentes para indizar estos datos.

Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md). Para obtener información conceptual sobre los controladores de filtro, vea [desarrollar controladores de filtro](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filtros y controladores de protocolo

Los controladores de protocolo proporcionan al indizador de Windows Search acceso a los almacenes de datos, lo que permite que el indexador Rastree los nodos de un almacén de datos y extraiga información relevante para el índice. Windows Search, por ejemplo, se suministra con controladores de protocolo para almacenes del sistema de archivos y para algunas versiones de ambos almacenes de datos de Microsoft Outlook. Al indizar el correo electrónico de Outlook, el controlador de protocolo rastrea todos los mensajes de un conjunto de carpetas de Outlook y extrae información de cada mensaje y datos adjuntos. Esta información se pasa al indexador para su inclusión en el catálogo de Windows Search.

Para obtener información general sobre el administrador de catálogos y el administrador de ámbito de rastreo (CSM), consulte [usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indexación de un formato de archivo compuesto

Un formato de archivo compuesto se puede indizar para que los elementos individuales del archivo puedan devolverse como resultados individuales. Un formato de archivo compuesto, como un archivo comprimido con la extensión de nombre de archivo. zip, es esencialmente un almacén de datos y se puede tratar como tal para fines de indexación. En el ejemplo siguiente se muestra un archivo. zip en el espacio de nombres del sistema de archivos (FILE://c:/test/test.zip) en el que hay subcarpetas y elementos individuales.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

El controlador de protocolo de archivo detecta cuándo FILE://c:/test/test.zip los cambios mediante la supervisión de los registros de cambios del sistema de archivos e invocará un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registrado para los archivos. zip en ese archivo cuando cambie el archivo, pero no tiene conocimiento de la estructura interna del archivo. zip.

Debe informar al indexador de que el formato de archivo compuesto es un almacén de datos. Es necesario hacerlo para los elementos individuales que se van a indizar y recuperar como entidades únicas. Después de haber implementado un origen de datos de Shell y realizado los pasos siguientes, tendrá un controlador de protocolo que puede procesar y exponer los datos de un formato de archivo compuesto (archivo. zip) como elementos individuales.

**Para informar al indizador de que un archivo compuesto es un almacén de datos:**

1.  Cree un controlador de protocolo (mediante [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) o [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) para los archivos. zip que tienen la capacidad de enlazar con el archivo de código fuente. Para obtener más información, vea [instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md).

    Por ejemplo, puede usar una ruta de acceso con escape al archivo. zip como el nombre de la carpeta raíz y, a continuación, usar una sintaxis de jerarquía como cualquier otro formato de archivo.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Con los datos de ejemplo anteriores de c: \\ test \\test.zip, las direcciones URL únicas serían las siguientes. Con estas direcciones URL, el controlador de protocolo tiene la información necesaria para enlazar con el archivo. zip y enumerar las direcciones URL secundarias, incluidos los archivos internos, para que se puedan enlazar y indexar mediante los filtros. doc y. txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Asegúrese de que el controlador de protocolo cumple las dos condiciones siguientes:
    -   Las direcciones URL raíz de un archivo. zip deben emitir PKEY \_ Search \_ IsClosedDirectory ([System. Search. IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) en las direcciones URL que son las direcciones URL del archivo. zip raíz. Por ejemplo,. zip:///FILE:%2f%2f%2fc:%2ftest% 2ftest.zip/debe emitir IsClosedDirectory = **true**. Esto indica al indizador que, si la fecha de esta dirección URL no ha cambiado, no necesita procesar ninguna de las direcciones URL secundarias.
    -   Cada dirección URL secundaria de esa dirección URL debe emitir PKEY \_ Search \_ IsFullyContained ([System. Search. IsFullyContained](../properties/props-system-search-isfullycontained.md)) en las direcciones URL secundarias de la dirección URL raíz. zip. Normalmente, al final de un rastreo incremental, el indexador trata todas las direcciones URL no visitadas como elementos que deben eliminarse. Pero el archivo. zip raíz no debe procesar las direcciones URL raíz porque no ha cambiado nada. Al emitir esta propiedad como **true** , se indica al indizador que si esta dirección URL no se ha procesado al final de un rastreo incremental, no se debe eliminar. Solo se eliminará si el elemento raíz ha cambiado y no se ha visitado.

Windows Search requiere una página de inicio para un protocolo con el fin de saber qué direcciones URL rastrearán de forma incremental y qué direcciones URL se deben omitir cuando se encuentren. Pero no podemos empezar con una dirección URL para cada archivo. zip, porque no sabemos dónde está cada archivo. zip. Por lo tanto, la dirección URL de la página de inicio del controlador del protocolo. zip debe ser capaz de enumerar todo en la raíz de las rutas de acceso de escape de todos los archivos. zip. Estos archivos. zip no tienen por qué estar en el espacio de nombres FILE: y podrían ser una dirección URL de tipo MAPI que apunte a un archivo. zip como datos adjuntos, por ejemplo.

**Para registrar una raíz como página de Inicio:**

1.  Registre una raíz como. zip:///como página de inicio para que todos los archivos. zip se inicien allí, en efecto. Al procesar el archivo root. zip: URL, el controlador de protocolo debe generar la lista de direcciones URL secundarias que se van a emitir consultando en Windows Search todas las direcciones URL con System. FileExtension = ". zip".
2.  Escapa a esas direcciones URL para quitar las barras diagonales y devolverlas como direcciones URL secundarias. Una consulta de ejemplo para recuperar los tipos que desea podría tener el aspecto siguiente.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Cuando Windows Search realiza periódicamente un rastreo incremental en la dirección URL raíz de. zip:///, debe reflejar la lista de direcciones URL que la búsqueda de Windows ya está manteniendo y que son direcciones URL. zip. Si se detecta una eliminación en el almacén nativo donde se almacena el archivo. zip, no aparece en la enumeración y se quita esa rama del árbol del archivo. zip.
4.  Para enlazar con los datos. zip de otro controlador de protocolo, lo ideal es pasar por el [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de esa dirección URL para enlazar con el almacenamiento del objeto y no suponer que siempre es un archivo. Esto le ofrece la flexibilidad de trabajar con datos adjuntos en almacenes de correo electrónico, por ejemplo.
5.  Cuando se emiten direcciones URL secundarias para cada archivo. zip, se debe usar PKEY \_ Search \_ UrlToIndexWithModificationTime ([System. Search. UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) para pasar PKEY \_ DateModified ([System. DateModified](../properties/props-system-datemodified.md)) del archivo. zip real para que el indexador rastree el archivo. zip solo si ha cambiado.

Para que las direcciones URL. zip se indexen inmediatamente después de que se creen o modifiquen, y no tengan que esperar un rastreo incremental para detectar su nuevo estado, podría supervisar el sistema de archivos por sí mismo para los cambios en el archivo. zip. Sin embargo, este enfoque no funcionaría en otros almacenes de datos como MAPI.

**Para que las direcciones URL de. zip se indexen cuando se crean o modifican:**

1.  Cree un filtro (y la implementación de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para el tipo de archivo. zip. Para obtener más información, vea [desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md).
2.  Cada vez que se llama a la implementación de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , se debe a que se ha detectado o modificado esa dirección URL. A continuación, genere un evento para la dirección URL. zip correspondiente a la dirección URL de origen, a través de la interfaz [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) . Esto le ofrece la posibilidad de indicar inmediatamente al indexador que hay nuevos datos que se van a indizar sin tener que esperar al rastreo incremental.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Código de ejemplo: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Controladores de protocolo de depuración](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
