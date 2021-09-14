---
description: Algunas aplicaciones almacenan sus elementos en bases de datos o tipos de archivo personalizados.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Descripción de los controladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363303"
---
# <a name="understanding-protocol-handlers"></a>Descripción de los controladores de protocolo

Algunas aplicaciones almacenan sus elementos en bases de datos o tipos de archivo personalizados. Aunque Windows Search puede indexar el nombre y las propiedades del archivo, Windows no tiene ningún conocimiento del contenido del archivo. Como resultado, estos elementos no se pueden indexar ni exponer en el shell Windows shell. Al crear un controlador de protocolo, puede hacer que estos elementos estén disponibles para la indexación. También puede indexar un formato de archivo compuesto, como un .zip archivo.

Este tema se organiza de la siguiente manera:

-   [Indexación de almacenes de datos con controladores de protocolo](#indexing-data-stores-with-protocol-handlers)
    -   [Almacenes de datos de Shell](#shell-data-stores)
    -   [Controladores de protocolo](#protocol-handlers)
    -   [Filtros y controladores de protocolo](#filters-and-protocol-handlers)
-   [Indexación de un formato de archivo compuesto](#indexing-a-compound-file-format)
-   [Temas relacionados](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexación de almacenes de datos con controladores de protocolo

Cuando los usuarios necesitan buscar bases de datos heredadas, almacenes de correo electrónico u otras estructuras de datos que no son compatibles con Windows Search, primero debe determinar si ya existe un controlador de protocolo para ese almacén de datos, quizás para su uso con otra aplicación como SharePoint Server. Si es así, puede instalar ese controlador de protocolo en el sistema. Windows Los controladores de protocolo de búsqueda usan especificaciones de diseño similares a SharePoint Server, y a menudo se pueden usar indistintamente.

Para obtener más información sobre la implementación de Search Server 2008 con Office SharePoint Server 2007, vea [Federated Search \[ Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Almacenes de datos de Shell

Antes de que un desarrollador externo de nuevos formatos de archivo y almacenes de datos pueda obtener esos formatos y almacenes para que aparezcan en los resultados de la consulta en Windows Explorer, el desarrollador debe implementar un origen de datos de Shell. Un origen de datos de Shell es un componente que se usa para ampliar el espacio de nombres de Shell y exponer elementos en un almacén de datos. Un almacén de datos es un repositorio de datos. Un almacén de datos se puede exponer al modelo de programación de Shell como un contenedor que usa un origen de datos de Shell. Los elementos de un almacén de datos se pueden indexar mediante el sistema Windows Search mediante un controlador de protocolo. El controlador de protocolo implementa el protocolo para acceder a un origen de contenido en su formato nativo. Las [**interfaces ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) se usan para implementar un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indexar.

Si desea que los resultados de la consulta aparezcan en Windows Explorer, debe implementar un origen de datos de Shell para poder crear un controlador de protocolo para ampliar el índice. Sin embargo, si todas las consultas se van a realizar mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, no es estrictamente necesario un espacio de nombres de Shell que sigue siendo el preferido.

> [!Note]  
> Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. A veces, un controlador se conoce como una extensión de Shell o un controlador de extensiones de Shell.

 

Si desea que los usuarios puedan ver sus resultados de búsqueda desde Windows Explorer, debe crear un controlador de protocolo y uno o varios de los siguientes complementos:

-   Controlador de menú contextual
-   Controlador de iconos
-   Otro tipo de controlador de archivos

Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando lograr, vea "Información general de los controladores" en [Windows Search como](-search-3x-wds-development-ovr.md)una plataforma de desarrollo . Para obtener información sobre cómo crear controladores, vea [Registering Shell Extensions](../shell/reg-shell-exts.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))y File [Type Handlers](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Controladores de protocolo

Si el almacén de datos también es un contenedor (por ejemplo, una carpeta del sistema de archivos), debe implementar un filtro para enumerar las direcciones URL del contenedor. Si el almacén de datos contiene datos o tipos de archivo distintos de uno de los 200 tipos de archivo admitidos por Windows Search, debe implementar un filtro para tener acceso e indexar el contenido de los elementos del almacén. Windows La búsqueda usa el controlador de [**protocolos y la tecnología IFilter**](/windows/win32/api/filter/nn-filter-ifilter) similar a la que usa SharePoint Server. Si ya tiene filtros para un almacén y un tipo de archivo específicos instalados en el sistema que se va a indexar, Windows Search puede usar las interfaces existentes para indexar estos datos.

Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md). Para obtener información conceptual sobre los controladores de filtro, vea [Developing Filter Handlers](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filtros y controladores de protocolo

Los controladores de protocolo dan al indexador Windows Search acceso a los almacenes de datos, lo que permite que el indexador rastree los nodos de un almacén de datos y extraiga información pertinente para indexar. Windows Busque, por ejemplo, que se distribuye con controladores de protocolo para los almacenes del sistema de archivos y para algunas versiones de los dos almacenes de datos Outlook Microsoft. Al indexar Outlook correo electrónico, el controlador de protocolo rastrea todos los mensajes de un conjunto de carpetas Outlook y extrae información de cada mensaje y datos adjuntos. Esta información se pasa al indexador para su inclusión en el catálogo Windows Search.

Para obtener información general sobre el Administrador de catálogos Administrador del ámbito de rastreo (CSM), vea Uso del Administrador de [catálogos](-search-3x-wds-mngidx-catalog-manager.md) y Uso [del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indexación de un formato de archivo compuesto

Se puede indexar un formato de archivo compuesto para que los elementos individuales del archivo se puedan devolver como resultados individuales. Un formato de archivo compuesto, como un archivo comprimido con una extensión de nombre de archivo .zip es básicamente un almacén de datos y se puede tratar como tal con fines de indexación. En el ejemplo siguiente se muestra .zip archivo en el espacio de nombres del sistema de archivos (FILE://c:/test/test.zip) en el que hay subcarpetas y elementos individuales.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

El controlador del protocolo FILE detecta cuando FILE://c:/test/test.zip cambia supervisando los registros de cambios del sistema de archivos e invocará un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registrado para los archivos .zip en ese archivo cuando cambie el archivo, pero no tiene conocimiento de la estructura interna del propio archivo .zip.

Debe informar al indexador de que el formato de archivo compuesto es un almacén de datos. Es necesario hacerlo para que los elementos individuales se indexe y se recuperen como entidades únicas. Después de implementar un origen de datos de Shell y realizar los pasos siguientes, tendrá un controlador de protocolo que puede procesar y exponer los datos de un formato de archivo compuesto (un archivo .zip) como elementos individuales.

**Para informar al indexador de que un archivo compuesto es un almacén de datos:**

1.  Cree un controlador de protocolo (mediante [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) o [**ISearchProtocol2)**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)para .zip que tenga la capacidad de enlazar al archivo de origen. Para obtener más información, vea [Installing and Registering Protocol Handlers](-search-3x-wds-ph-install-registration.md).

    Por ejemplo, podría usar una ruta de acceso con escape al archivo .zip como nombre de carpeta raíz y, a continuación, usar una sintaxis de jerarquía como cualquier otro formato de archivo.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Con los datos de ejemplo anteriores para c: \\ test \\test.zip, las direcciones URL únicas serían las siguientes. Con estas direcciones URL, el controlador de protocolo tiene la información necesaria para enlazar al archivo .zip y enumerar las direcciones URL secundarias, incluidos los archivos internos, para que se puedan enlazar e indexar mediante los filtros .doc y .txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Asegúrese de que el controlador de protocolo cumple las dos condiciones siguientes:
    -   Las direcciones URL raíz de un archivo .zip deben emitir PKEY \_ Search \_ IsClosedDirectory ([System.Search.IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) en las direcciones URL que son las direcciones URL raíz .zip archivo. Por ejemplo, .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ debe emitir IsClosedDirectory = **TRUE**. Esto indica al indexador que, si la fecha de esta dirección URL no ha cambiado, no es necesario procesar ninguna de las direcciones URL secundarias.
    -   Cada dirección URL secundaria de esa dirección URL debe emitir PKEY \_ Search \_ IsFullyContained ([System.Search.IsFullyContained](../properties/props-system-search-isfullycontained.md)) en las direcciones URL secundarias de la dirección URL .zip raíz. Normalmente, al final de un rastreo incremental, el indexador trata todas las direcciones URL no vistas como elementos que se deben eliminar. Pero el archivo raíz .zip no debe procesar las direcciones URL raíz porque no ha cambiado nada. La emisión de esta propiedad como **TRUE** indica al indexador que si esta dirección URL no se ha procesado al final de un rastreo incremental, no se debe eliminar. Solo se eliminará si el elemento raíz ha cambiado y no se visita.

Windows La búsqueda requiere una página de inicio para un protocolo con el fin de saber qué direcciones URL rastrear de forma incremental y qué direcciones URL se deben omitir cuando se encuentran. Pero no podemos empezar con una dirección URL para cada archivo .zip, porque no sabemos dónde está cada .zip archivo. Por lo tanto, .zip dirección URL de la página de inicio del controlador de protocolos debe ser capaz de enumerar todo lo que se encuentra en la raíz de las rutas de acceso con escape de todos los .zip archivos. Esos .zip no están necesariamente en el espacio de nombres FILE: y podrían ser una dirección URL de tipo MAPI que apunta a un archivo .zip como datos adjuntos, por ejemplo.

**Para registrar una raíz como página de inicio:**

1.  Registre una raíz como .zip:/// como página de inicio para que todos los archivos .zip se inicien allí, en efecto. Al procesar la dirección URL .zip: raíz, el controlador de protocolo debe generar la lista de direcciones URL secundarias que se emitirán consultando Windows Search para todas las direcciones URL con System.FileExtension = ".zip".
2.  Escape esas direcciones URL para quitar las barras diagonales y devolverlas como direcciones URL secundarias. Una consulta de ejemplo para recuperar los tipos que desea podría tener el siguiente aspecto.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Cuando Windows Search realiza periódicamente un rastreo incremental en la dirección URL raíz de .zip:///, debe reflejar de nuevo la lista de direcciones URL que Windows Search ya mantiene y que .zip url. Si se detecta una eliminación en el almacén nativo donde se almacena el archivo .zip, no aparece en la enumeración y se quita esa rama del árbol del .zip.
4.  Para enlazar a los datos de .zip para otro controlador de protocolo, lo ideal es pasar por [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para que esa dirección URL se enlace al almacenamiento del objeto y no suponer que siempre es un archivo. Esto le ofrece la flexibilidad de trabajar con datos adjuntos en almacenes de correo electrónico, por ejemplo.
5.  Al emitir direcciones URL secundarias para cada archivo .zip, debe usar PKEY \_ Search \_ UrlToIndexWithModificationTime ([System.Search.UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) para pasar PKEY \_ [DateModified ( System.DateModified)](../properties/props-system-datemodified.md)del archivo .zip real para que el indexador rastree el archivo .zip solo si ha cambiado.

Para que las direcciones URL de .zip se indexen inmediatamente después de que se creen o modifiquen, y no tengan que esperar a que un rastreo incremental detecte su nuevo estado, podría supervisar el sistema de archivos por sí mismo para .zip cambios de archivo. Sin embargo, este enfoque no funcionaría para otros almacenes de datos, como MAPI.

**Para que las direcciones URL .zip se indexe cuando se creen o modifiquen:**

1.  Cree un filtro (e implementación de la [**interfaz IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) para el tipo .zip archivo. Para obtener más información, vea [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).
2.  Cada vez que se llama a la implementación de [**IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) se debe a que esa dirección URL se ha detectado o cambiado. A continuación, genere un evento para la dirección URL de .zip adecuada para la dirección URL de origen, a través de la [**interfaz IGatherNotifyInline.**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) Si lo hace, podrá decir inmediatamente al indexador que hay nuevos datos que indexar sin tener que esperar al rastreo incremental.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notificación al índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Ejemplo de código: Extensiones de shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuración de controladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
