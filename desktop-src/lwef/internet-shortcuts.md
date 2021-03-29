---
title: Accesos directos a Internet
description: El objeto de acceso directo a Internet se usa para crear accesos directos de escritorio a sitios de Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Objetos de acceso directo de Internet
- Controles WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077717"
---
# <a name="internet-shortcuts"></a>Accesos directos a Internet

El objeto de acceso directo a Internet se usa para crear accesos directos de escritorio a sitios de Internet. Al igual que los accesos directos a los elementos del sistema de archivos, los accesos directos a Internet adoptan la forma de un icono en el escritorio. Cuando el usuario hace clic en el icono, se inicia el explorador y muestra el sitio asociado con el acceso directo.

Se tratan los temas siguientes.

-   [Crear accesos directos a Internet](#creating-internet-shortcuts)
    -   [Crear un acceso directo a Internet desde un control WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Crear un acceso directo a Internet desde una dirección URL](#creating-an-internet-shortcut-from-a-url)
-   [Acceso al almacenamiento de propiedades](#accessing-property-storage)
-   [Interfaces](#interfaces)
    -   [interfaces OLE](#ole-interfaces)
    -   [Interfaces de Shell](#shell-interfaces)
-   [Funciones](#functions)
    -   [Funciones de la utilidad de acceso directo de Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Crear accesos directos a Internet

Puede crear un acceso directo a Internet mediante un control WebBrowser o con la dirección URL de la página.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Crear un acceso directo a Internet desde un control WebBrowser

Si la aplicación hospeda un control WebBrowser, puede usar el objeto de acceso directo a Internet para crear accesos directos de la siguiente manera.

1.  Cree una instancia del objeto de acceso directo a Internet con [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)mediante un identificador de clase (CLSID) de CLSID \_ InternetShortcut.
2.  Pase el puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del WebBrowser al objeto de acceso directo a Internet con [IObjectWithSite:: SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Llame al método [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) del objeto de acceso directo de Internet cuando desee crear un acceso directo a la página que está viendo el control WebBrowser.

Se creará un acceso directo en la ubicación especificada en [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). Esta ubicación permite que el control WebBrowser restaure su estado, que incluye la tarea de cargar los documentos correctos en conjuntos de Marcos.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Crear un acceso directo a Internet desde una dirección URL

También puede crear un acceso directo a Internet si tiene la dirección URL de la página a la que desea vincular.

1.  Cree una instancia del objeto de acceso directo a Internet con [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)mediante un CLSID de CLSID \_ InternetShortcut.
2.  Use el método [IUniformResourceLocator:: SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) para establecer la dirección URL en el acceso directo.
3.  Use el método [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el archivo de acceso directo en una ubicación deseada.

## <a name="accessing-property-storage"></a>Acceso al almacenamiento de propiedades

El objeto de acceso directo a Internet contiene varias propiedades a las que se puede tener acceso a través de la interfaz [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) del objeto con el procedimiento siguiente.

1.  Obtenga la interfaz [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) llamando a [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IPropertySetStorage.
2.  Para obtener acceso al conjunto de almacenamiento de propiedades de acceso directo a Internet, llame a [IPropertySetStorage:: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) con FMTID \_ Intshcut o FMTID \_ InternetSite para obtener la interfaz [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) .
3.  Lea la información de almacenamiento de propiedades con [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) pasando el identificador de propiedad adecuado.

Con la [versión 4,70 o superior](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) de Shell32.dll, también puede recuperar la interfaz [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) llamando a [**IShellFolder:: BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) con el parámetro *PIDL* establecido en. Archivo URL y el parámetro *riid* establecido en IID \_ IPropertySetStorage.

Se pueden solicitar los siguientes identificadores de propiedad para FMTID \_ Intshcut.



| PROPID               | Tipo Variant | Descripción                                 |
|----------------------|--------------|---------------------------------------------|
| el PID \_ es una \_ dirección URL         | VT \_ LPWStr   | Dirección URL a la que se dirige el acceso directo             |
| \_el PID es \_ Name        | VT \_ LPWStr   | Nombre del acceso directo a Internet               |
| el PID \_ es \_ WORKINGDIR  | VT \_ LPWStr   | Directorio de trabajo para el acceso directo          |
| el PID \_ es \_ Hotkey      | VT \_ UI2      | Tecla de acceso rápido para el acceso directo                     |
| el PID \_ es \_ SHOWCMD     | VT \_ I4       | Mostrar comando para acceso directo                   |
| el PID \_ es \_ ICONINDEX   | VT \_ I4       | Índice del icono                           |
| el PID \_ es \_ IconFile    | VT \_ LPWStr   | Archivo que contiene el icono                 |
| el PID \_ es \_ novedades    | VT \_ LPWStr   | Nuevo texto                             |
| el PID \_ es \_ autor      | VT \_ LPWStr   | Autor                                      |
| Descripción del PID \_ \_ | VT \_ LPWStr   | Texto descriptivo del sitio                    |
| el PID \_ es un \_ Comentario     | VT \_ LPWStr   | Comentario de usuario anotado                      |
| el PID \_ es \_ roaming      | VT \_ bool     | True cuando el acceso directo se mueve por primera vez |



 

Se pueden solicitar los siguientes identificadores de propiedad para FMTID \_ InternetSite.



| PROPID                     | Tipo Variant | Descripción                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ novedades     | VT \_ LPWStr   | Nuevo texto                                   |
| \_INTSITE \_ autor de PID       | VT \_ LPWStr   | Autor                                            |
| PID \_ INTSITE \_ LASTVISIT    | VT \_ FILETIME | Hora de la última visita del sitio                        |
| PID \_ INTSITE \_ LASTMOD      | VT \_ FILETIME | Hora de la última modificación del sitio                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | Número de veces que el usuario ha visitado                  |
| Descripción de PID \_ INTSITE \_  | VT \_ LPWStr   | Texto descriptivo del sitio                          |
| Comentario de PID \_ INTSITE \_      | VT \_ LPWStr   | Comentario de usuario anotado                            |
| \_indicadores INTSITE de PID \_        | VT \_ UI4      | Indica el uso de \_ marcas PIDISF (vea más abajo)       |
| PID \_ INTSITE \_ CONTENTLEN   | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ RECURSE      | N/D          | No se admite actualmente.                           |
| \_Ver PID INTSITE \_        | N/D          | No se admite actualmente.                           |
| suscripción de PID \_ INTSITE \_ | VT \_ UI8      | Valor de SUBSCRIPTIONCOOKIE para el administrador de suscripciones |
| \_ \_ dirección URL de PID INTSITE          | VT \_ LPWStr   | Dirección URL a la que se dirige el acceso directo                   |
| \_título INTSITE de PID \_        | VT \_ LPWStr   | Title                                             |
| Página de códigos de PID \_ INTSITE \_     | VT \_ UI4      | Página de códigos del documento                          |
| seguimiento de PID \_ INTSITE \_     | N/D          | No se admite actualmente.                           |
| PID \_ INTSITE \_ ICONINDEX    | VT \_ I4       | Índice del icono                                 |
| PID \_ INTSITE \_ IconFile     | VT \_ LPWStr   | Archivo que contiene el icono                       |
| PID \_ INTSITE \_ móvil       | VT \_ UI4      | La entrada se agregó debido a itinerancia                |



 

A continuación se muestran las marcas de sitios de Internet.



| Marca                    | Descripción                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ RECENTLYCHANGED | Indica que se ha cambiado recientemente un sitio |
| PIDISF \_ CACHEDSTICKY    | No se admite actualmente.                    |
| PIDISF \_ CACHEIMAGES     | No se admite actualmente.                    |
| PIDISF \_ FOLLOWALLLINKS  | No se admite actualmente.                    |



 

Los valores siguientes se usan para el historial de itinerancia de Internet.



| Valor de PID \_ INTSITE \_ móvil         | Descripción                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor no establecido o PIDISR \_ actualizado \_ \_ | Esta entrada de caché no se ha modificado mediante itinerancia.                                                                                                                       |
| PIDISR \_ necesita \_ Agregar                    | Esta entrada de caché se ha agregado a la memoria caché mediante itinerancia. Establecer PIDISR \_ actualizada \_ \_ una vez que se complete el procesamiento de la entrada.                                                   |
| PIDISR \_ necesita \_ actualizarse                 | Esta entrada de caché ya existía en el equipo local, pero se actualizó mediante itinerancia. Establecer PIDISR \_ actualizada \_ \_ una vez que se complete el procesamiento de la entrada.                 |
| PIDISR \_ necesita \_ eliminar                 | La itinerancia detectó que se debe eliminar esta entrada de caché. Por ejemplo, es posible que el usuario haya desactivado el historial del explorador. Elimine la entrada mediante DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfaces

El objeto de acceso directo a Internet expone varias interfaces.

### <a name="ole-interfaces"></a>interfaces OLE

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Interfaces de Shell

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Functions

Hay varias funciones de utilidad que se pueden utilizar con el objeto de acceso directo a Internet.

### <a name="internet-shortcut-utility-functions"></a>Funciones de la utilidad de acceso directo de Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 