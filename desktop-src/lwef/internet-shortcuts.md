---
title: Accesos directos a Internet
description: El objeto de acceso directo de Internet se usa para crear accesos directos de escritorio a sitios de Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Objetos de acceso directo de Internet
- Controles WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aba53c320ed740fe7d91a2425b4d47d66e28d78aa35e4ce893efeed12380c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749413"
---
# <a name="internet-shortcuts"></a>Accesos directos a Internet

El objeto de acceso directo de Internet se usa para crear accesos directos de escritorio a sitios de Internet. Al igual que los accesos directos a los elementos del sistema de archivos, los accesos directos a Internet toman la forma de un icono en el escritorio. Cuando el usuario hace clic en el icono, se inicia el explorador y muestra el sitio asociado al acceso directo.

Se tratan los temas siguientes.

-   [Creación de accesos directos de Internet](#creating-internet-shortcuts)
    -   [Crear un acceso directo a Internet desde un control WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Creación de un acceso directo a Internet a partir de una dirección URL](#creating-an-internet-shortcut-from-a-url)
-   [Acceso a la propiedad Storage](#accessing-property-storage)
-   [Interfaces](#interfaces)
    -   [interfaces OLE](#ole-interfaces)
    -   [Interfaces de shell](#shell-interfaces)
-   [Funciones](#functions)
    -   [Funciones de la utilidad de acceso directo de Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Creación de accesos directos de Internet

Puede crear un acceso directo a Internet mediante un control WebBrowser o con la dirección URL de la página.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Crear un acceso directo a Internet desde un control WebBrowser

Si la aplicación hospeda un control WebBrowser, puede usar el objeto de acceso directo de Internet para crear accesos directos de la siguiente manera.

1.  Cree una instancia del objeto de acceso directo de Internet [con CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)mediante un identificador de clase (CLSID) de CLSID \_ InternetShortcut.
2.  Pase el puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) de WebBrowser al objeto de acceso directo de Internet [con IObjectWithSite::SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Llame al método [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) del objeto de acceso directo de Internet cuando desee crear un acceso directo a la página que está visualizando el control WebBrowser.

Se creará un acceso directo en la ubicación especificada en [IPersistFile::Save.](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) Esta ubicación permite que el control WebBrowser restaure su estado, lo que incluye la tarea de cargar los documentos correctos en conjuntos de fotogramas.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Creación de un acceso directo a Internet a partir de una dirección URL

También puede crear un acceso directo a Internet si tiene la dirección URL de la página a la que desea vincular.

1.  Cree una instancia del objeto de acceso directo de Internet [con CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), mediante un CLSID de CLSID \_ InternetShortcut.
2.  Use el [método IUniformResourceLocator::SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) para establecer la dirección URL en el acceso directo.
3.  Use el [método IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el archivo de acceso directo en una ubicación deseada.

## <a name="accessing-property-storage"></a>Acceso a la propiedad Storage

El objeto de acceso directo de Internet contiene varias propiedades a las que se puede acceder a través de la interfaz [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) del objeto con el procedimiento siguiente.

1.  Obtenga la [interfaz IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) llamando a [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IPropertySetStorage.
2.  Acceda al conjunto de almacenamiento de propiedades de acceso directo de Internet llamando a [IPropertySetStorage::Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) con FMTID Intshcut o FMTID InternetSite para obtener la \_ \_ interfaz [IPropertyStorage.](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)
3.  Lea la información de almacenamiento de propiedades [con IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) pasando el identificador de propiedad adecuado.

Con [la versión 4.70](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) o posterior de Shell32.dll, también puede recuperar la interfaz [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) llamando a [**IShellFolder::BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) con el parámetro *pidl* establecido en . Archivo URL y el *parámetro riid* establecido en IID \_ IPropertySetStorage.

Se pueden solicitar los siguientes IDs de propiedad para FMTID \_ Intshcut.



| PROPID               | Tipo de variante | Descripción                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ IS \_ URL         | VT \_ LPWSTR   | Dirección URL a la que el acceso directo dirige             |
| PID \_ ES \_ NAME        | VT \_ LPWSTR   | Nombre del acceso directo a Internet               |
| PID \_ ESTÁ \_ FUNCIONANDODIR  | VT \_ LPWSTR   | Directorio de trabajo para el acceso directo          |
| PID \_ IS \_ HOTKEY      | VT \_ UI2      | Tecla de acceso rápido para el acceso directo                     |
| PID \_ IS \_ SHOWCMD     | VT \_ I4       | Mostrar comando para acceso directo                   |
| PID \_ IS \_ ICONINDEX   | VT \_ I4       | Índice del icono                           |
| PID \_ IS \_ ICONFILE    | VT \_ LPWSTR   | Archivo que contiene el icono                 |
| PID \_ IS \_ WHATSNEW    | VT \_ LPWSTR   | Texto de novedades                             |
| PID \_ ES \_ EL AUTOR      | VT \_ LPWSTR   | Autor                                      |
| PID \_ IS \_ DESCRIPTION | VT \_ LPWSTR   | Texto de descripción del sitio                    |
| PID \_ IS \_ COMMENT     | VT \_ LPWSTR   | Comentario anotado por el usuario                      |
| PID \_ ESTÁ \_ DESANCHADO      | VT \_ BOOL     | True cuando el acceso directo se recorre por primera vez |



 

Se pueden solicitar los siguientes IDs de propiedad para FMTID \_ InternetSite.



| PROPID                     | Tipo de variante | Descripción                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ WHATSNEW     | VT \_ LPWSTR   | Texto de novedades                                   |
| PID \_ INTSITE \_ AUTHOR       | VT \_ LPWSTR   | Autor                                            |
| PID \_ INTSITE \_ LASTVISIT    | VT \_ FILETIME | Hora en que se visitó por última vez el sitio                        |
| PID \_ INTSITE \_ LASTMOD      | VT \_ FILETIME | Hora en que se modificó por última vez el sitio                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | Número de veces que el usuario ha visitado                  |
| PID \_ INTSITE \_ DESCRIPTION  | VT \_ LPWSTR   | Texto de descripción del sitio                          |
| PID \_ INTSITE \_ COMMENT      | VT \_ LPWSTR   | Comentario anotado por el usuario                            |
| MARCAS \_ DE PID INTSITE \_        | VT \_ UI4      | Indica el uso de marcas DE SESF \_ (consulte a continuación)       |
| PID \_ INTSITE \_ CONTENTLEN   | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ RECURSE      | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ WATCH        | N/D          | No se admite actualmente.                           |
| SUSCRIPCIÓN \_ A PID \_ INTSITE | VT \_ UI8      | Valor SUBSCRIPTIONCOOKIE para el administrador de suscripciones |
| PID \_ INTSITE \_ URL          | VT \_ LPWSTR   | Dirección URL a la que dirige el acceso directo                   |
| PID \_ INTSITE \_ TITLE        | VT \_ LPWSTR   | Título                                             |
| PID \_ INTSITE \_ CODEPAGE     | VT \_ UI4      | Página de códigos del documento                          |
| SEGUIMIENTO \_ DE PID INTSITE \_     | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ ICONINDEX    | VT \_ I4       | Índice del icono                                 |
| PID \_ INTSITE \_ ICONFILE     | VT \_ LPWSTR   | Archivo que contiene el icono                       |
| PID \_ INTSITE \_ ROAMED       | VT \_ UI4      | La entrada se agregó debido a la itinerancia.                |



 

Las siguientes son las marcas del sitio de Internet.



| Marca                    | Descripción                                |
|-------------------------|--------------------------------------------|
| SE HA MODIFICADO \_ RECIENTEMENTE. | Indica que un sitio se ha cambiado recientemente |
| SE HA ALMACENADO \_ EN CACHÉSTICKY    | No se admite actualmente.                    |
| SESF \_ CACHEIMAGES     | No se admite actualmente.                    |
| LE \_ SIGUESFALLLINKS  | No se admite actualmente.                    |



 

Los valores siguientes se usan para el historial de itinerancia de Internet.



| Valor de PID \_ INTSITE \_ ROAMED         | Descripción                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor no establecido o SE HA \_ ACTUALIZADO \_ \_ | La itinerancia no ha modificado esta entrada de caché.                                                                                                                       |
| SE NECESITA \_ AGREGAR. \_                    | Esta entrada de caché se agregó a la memoria caché en itinerancia. Establezca SESR UP TO DATE una vez que se complete el procesamiento \_ \_ de la \_ entrada.                                                   |
| LA ACTUALIZACIÓN DE SE \_ NECESITA \_                 | Esta entrada de caché ya existía en el equipo local, pero se actualizó en itinerancia. Establezca SESR UP TO DATE una vez que se complete el procesamiento \_ \_ de la \_ entrada.                 |
| SE NECESITA \_ ELIMINAR. \_                 | La itinerancia detectó que se debe eliminar esta entrada de caché. Por ejemplo, es posible que el usuario haya borrado su historial del explorador. Elimine la entrada mediante DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfaces

El objeto de acceso directo de Internet expone varias interfaces.

### <a name="ole-interfaces"></a>interfaces OLE

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [Ipersiststream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Interfaces de shell

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Functions

Hay varias funciones de utilidad que se pueden usar con el objeto de acceso directo de Internet.

### <a name="internet-shortcut-utility-functions"></a>Funciones de la utilidad de acceso directo de Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 