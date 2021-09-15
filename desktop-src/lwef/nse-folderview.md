---
title: Implementación de una vista de carpetas
description: Windows Shell proporciona una implementación predeterminada de la vista de carpeta, conocida de forma coloquial como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- objeto de vista de carpeta
- IShellView
- IShellBrowser, objetos de vista de carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568713"
---
# <a name="implementing-a-folder-view"></a>Implementación de una vista de carpetas

Windows Shell proporciona una implementación predeterminada de la vista de carpeta, conocida de forma coloquial como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres. Dado que algunas características de vista no se pueden lograr a través de vistas personalizadas, a menudo se recomienda usar el objeto de vista de carpeta del sistema predeterminado en lugar de una vista personalizada. Para obtener más información, [**vea SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). En el resto de este tema se describe la implementación de una vista de carpeta personalizada que no admite características de vista más recientes.

A diferencia de la vista de árbol, Windows Explorer no administra el contenido de una vista de carpeta. En su lugar, la ventana de vista de carpetas hospeda una ventana secundaria proporcionada por el objeto de carpeta. El objeto de carpeta es responsable de crear un objeto de vista de carpeta para mostrar el contenido de la carpeta en la ventana secundaria.

La clave para implementar un objeto de vista de carpeta es la [**interfaz IShellView.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) Esta interfaz la usa Windows Explorer para comunicarse con el objeto de vista de carpeta. Antes de mostrar una vista de carpeta, Windows Explorer llama al método [**IShellFolder::CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) del objeto de carpeta con *riid* establecido en IID \_ IShellView. Cree un objeto de vista de carpeta y devuelva su **interfaz IShellView.** A continuación, el objeto de vista de carpeta debe crear una ventana secundaria de la ventana de vista de carpetas y usar la ventana secundaria para mostrar información sobre el contenido de la carpeta.

Además de controlar cómo se muestran los datos, las extensiones también pueden personalizar varias de las características de Windows Explorer. Por ejemplo, una extensión puede agregar elementos a la barra de herramientas o barra de menús, o mostrar información sobre la barra de estado.

-   [El objeto de vista de carpeta](#the-folder-view-object)
-   [Inicialización del objeto de vista de carpeta](#initializing-the-folder-view-object)
-   [Mostrar la vista de carpetas](#displaying-the-folder-view)
-   [Implementación de IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [Actualizar](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [Uso de IShellBrowser para comunicarse con Windows Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Modificar la barra de menús Windows Explorer](#modifying-the-windows-explorer-menu-bar)
    -   [Modificar la barra de herramientas Windows Explorer](#modifying-the-windows-explorer-toolbar)
    -   [Modificar la barra de estado Windows Explorer](#modifying-the-windows-explorer-status-bar)
    -   [Almacenamiento de información específica de la vista](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>El objeto de vista de carpeta

Un objeto de vista de carpeta es un objeto De modelo de objetos componentes (COM) que expone una [**interfaz IShellView.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) Este objeto es responsable de:

-   Crear una ventana secundaria de la ventana de vista de carpeta y usarlo para mostrar el contenido de la carpeta.
-   Control de la comunicación con Windows Explorer.
-   Agregar comandos específicos de carpeta a la barra de menús Windows Explorer y a la barra de herramientas, y controlar esos comandos cuando se seleccionan.
-   Administrar la interacción del usuario con la ventana de vista de carpetas, como mostrar menús contextuales o controlar operaciones de arrastrar y colocar.

En este documento se de abordan los tres primeros temas. Dado que la interacción del usuario con la vista de carpeta tiene lugar dentro de la ventana secundaria, el objeto de vista de carpeta es responsable de controlarlo como lo haría con cualquier otra ventana.

Windows El explorador solicita un objeto de vista de carpeta mediante una llamada a [**IShellFolder::CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) del objeto de carpeta con *riid* establecido en IID \_ IShellView. El procedimiento para crear una vista de carpeta es:

1.  El objeto de carpeta crea una nueva instancia del objeto de vista de carpeta y devuelve un puntero a su [**interfaz IShellView.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview)
2.  Windows El Explorador inicializa el objeto de vista de carpeta llamando al [**método IShellView::CreateViewWindow.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) Cree una ventana secundaria de la ventana de vista de carpetas y devuelva su identificador a Windows Explorer.
3.  El objeto de vista de carpeta usa la interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) Windows Explorer para personalizar la barra de herramientas de Windows Explorer, la barra de menús y la barra de estado.
4.  El objeto de vista de carpeta muestra el contenido de la carpeta en la ventana secundaria.
5.  El objeto de vista de carpeta controla la interacción del usuario con la vista de carpeta y cualquier elemento de barra de herramientas o barra de menús específico de la carpeta.

## <a name="initializing-the-folder-view-object"></a>Inicialización del objeto de vista de carpeta

Windows El Explorador inicializa el objeto de vista de carpeta llamando al [**método IShellView::CreateViewWindow.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) Los parámetros del método proporcionan al objeto de vista de carpeta la información que necesita para crear la ventana secundaria que se usará para mostrar el contenido de la carpeta:

-   Puntero a la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) del objeto de vista de carpeta anterior. Este parámetro se puede establecer en **NULL.**
-   Estructura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) que contiene la configuración de la vista de carpeta anterior.
-   Puntero a la interfaz Windows Explorer [**IShellBrowser.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser)
-   Estructura [RECT](/previous-versions//ms536136(v=vs.85)) con las dimensiones de la ventana de vista de carpetas.

Se [**llama al método IShellView::CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) antes de destruir el objeto de vista de carpeta anterior. El [**puntero de interfaz IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) le permite comunicarse con el objeto de vista de carpeta anterior. Esta interfaz es principalmente útil si la carpeta anterior pertenecía a la extensión y usaba el mismo esquema de presentación. Si es así, puede comunicarse con el objeto de vista de carpeta anterior para fines como intercambiar la configuración privada.

Una manera sencilla de determinar si el puntero [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) pertenece a la extensión es hacer que todos los objetos de vista de carpeta exponán una interfaz privada. Llame [a IShellView::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar la interfaz privada y examine el valor devuelto para determinar si el objeto de vista de carpeta es uno de los que tiene. A continuación, puede usar un método privado en esa interfaz para intercambiar información.

La [**estructura FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) contiene la configuración de visualización de la vista de carpeta anterior. La configuración principal es el modo de visualización: icono grande, icono pequeño, lista o detalles. También hay una marca que contiene la configuración de una variedad de opciones de visualización, como si la vista debe alinearse a la izquierda. La presentación de la carpeta debe seguir esta configuración en la medida de lo posible para proporcionar a los usuarios una experiencia coherente a medida que van de una carpeta a otra. Debe almacenar esta estructura y actualizarla a medida que cambie la configuración. Windows El explorador [**llama a IShellView::GetCurrentInfo para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) obtener el valor más reciente de esta estructura antes de abrir la siguiente vista de carpeta.

La [**interfaz IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) se expone mediante Windows Explorer. Esta interfaz es complementaria a [**IShellView y**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) permite que un objeto de vista de carpeta se comunique con Windows Explorer. No hay otra manera de recuperar este puntero de interfaz, por lo que el objeto de vista de carpeta debe almacenarlo para su uso posterior. En concreto, deberá llamar a [IShellBrowser::GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para recuperar la ventana de vista de carpeta primaria que usará para crear la ventana secundaria. Tenga en cuenta que el método IShellBrowser::GetWindow no se incluye en la documentación de **IShellBrowser** porque se hereda de [IOleWindow.](/windows/win32/api/oleidl/nn-oleidl-iolewindow) Después de almacenar el puntero de interfaz, recuerde llamar a [IShellBrowser::AddRef para](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementar el recuento de referencias de la interfaz. Cuando ya no necesite la interfaz, llame a [IShellBrowser::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

Para crear la ventana secundaria:

1.  Examine las [**estructuras FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) [y RECT.](/previous-versions//ms536136(v=vs.85))
2.  Si es necesario, obtenga la configuración privada del objeto de vista de carpeta anterior.
3.  Llame [a IShellBrowser::GetWindow para](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) recuperar la ventana de vista de carpeta primaria.
4.  Cree un elemento secundario de la ventana de vista de carpetas obtenido en el paso anterior y vuelva a Windows Explorador.

## <a name="displaying-the-folder-view"></a>Mostrar la vista de carpetas

Una vez que haya creado la ventana secundaria y la haya devuelto Windows Explorer, puede mostrar el contenido de la carpeta. Normalmente, las extensiones muestran su información haciendo que la ventana secundaria hospeda un [control de vista](../controls/list-view-control-reference.md) de lista o un control **WebBrowser**. El control de vista de lista permite replicar la vista Windows explorer [clásico.](web-view.md) El control WebBrowser permite usar un documento HTML dinámico (DHTML) para mostrar la información, de forma muy parecido a la vista web Windows Explorer. Para obtener más información, consulte la documentación de esos controles.

La ventana de vista de carpetas siempre existe, incluso si no tiene el foco. Por lo tanto, debe mantener tres estados para la ventana secundaria:

-   Activado con el foco. La vista de carpeta se ha creado y tiene el foco. Establezca la barra de menús o los elementos de la barra de herramientas que sean adecuados para un estado centrado.
-   Activado sin foco. La vista de carpeta se ha creado y está activa, pero no tiene el foco. Establezca la barra de menús o los elementos de la barra de herramientas que sean adecuados para un estado no centrado. Omita los elementos que se aplican a la selección de elementos dentro de la vista de carpeta.
-   Desactivado. La vista de carpeta está a punto de destruirse. Quite todos los elementos de menú específicos de la carpeta.

Windows El Explorador notifica al objeto de vista de carpeta cuando cambia el estado de la ventana mediante una llamada a [**IShellView::UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate). A su vez, el objeto de vista de carpeta debe notificar a Windows Explorer cuando un usuario active la ventana de vista de carpetas mediante una llamada a [**IShellBrowser::OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive). Para obtener más información sobre esta interfaz, vea [Uso de IShellBrowser para comunicarse con Windows Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer).

Mientras la vista de carpetas está activa, debe procesar cualquier mensaje Windows, como [WM \_ SIZE](../winmsg/wm-size.md), que pertenezcan a la ventana secundaria. El procedimiento de ventana también recibirá mensajes [WM \_ COMMAND](../menurc/wm-command.md) para los elementos que haya agregado a la barra de menús o barra de herramientas Windows Explorer.

Después de crear la vista de carpeta, Windows Explorer llama a la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) del objeto de vista de carpeta para pasar una variedad de información. El objeto debe modificar su presentación en consecuencia. Cuando la vista de carpeta está a punto de destruirse, Windows Explorer notifica al objeto de vista de carpeta llamando a su [**método IShellView::D estroyViewWindow.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow)

## <a name="implementing-ishellview"></a>Implementación de IShellView

Una vez creado el objeto de carpeta, Windows Explorer llama a varios métodos [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) para solicitar información o notificar al objeto un cambio en el estado de Windows Explorer. En esta sección se describe cómo implementar esos **métodos IShellView.** Los métodos restantes se usan con fines más especializados, como el cuadro de diálogo Común Abrir archivo. Para más información, consulte la **documentación de IShellView.**

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

Cuando un usuario selecciona **Opciones** de carpeta en el menú herramientas de Windows **Explorer,** se muestra una hoja de propiedades que permite al usuario modificar las opciones de carpeta. Windows El Explorador llama al método [**IShellView::AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) del objeto de vista de carpeta para permitirle agregar una página a esta hoja de propiedades.

Windows El Explorador pasa un puntero a una función de devolución de llamada [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) en el parámetro *lpfn* de [**IShellView::AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Llame [a CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) para crear la página y, a continuación, llame a AddPropSheetPageProc para agregarla a la hoja de propiedades. Para obtener más información sobre cómo controlar las hojas de propiedades, vea [Hojas de propiedades](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>GetCurrentInfo

Cuando el usuario cambia de una carpeta a otra, Windows Explorer intenta mantener una vista de carpeta similar. Por ejemplo, si la vista de carpeta anterior mostraba iconos grandes, la siguiente también debería. Cuando Windows Explorer llama a [**IShellView::CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) para inicializar el objeto de vista de carpeta, el método recibe una [**estructura FOLDERSETTINGS.**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) Esta estructura contiene información que le permite hacer que la vista de carpeta sea coherente con la vista de carpeta anterior.

Para asegurarse de que la vista siguiente es coherente con la vista actual, almacene la [**estructura FOLDERSETTINGS.**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) Si la vista cambia, por ejemplo de iconos grandes a pequeños, actualice la estructura en consecuencia. Antes de cambiar de vista, Windows Explorer llamará a [**IShellView::GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) para solicitar los valores **FOLDERSETTINGS** actuales para pasarlos al siguiente objeto de vista de carpeta.

### <a name="refresh"></a>Actualizar

El usuario puede asegurarse de que la vista de carpeta  refleja  el estado actual de la carpeta seleccionando Actualizar en el menú Ver o presionando la tecla F5. Cuando el usuario lo hace, Windows Explorer llama al [**método IShellView::Refresh.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) El objeto de vista de carpeta debe actualizar inmediatamente la visualización de la vista de carpeta.

### <a name="saveviewstate"></a>SaveViewState

Windows El Explorador llama al [**método IShellView::SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) para solicitar al objeto de vista de carpeta que guarde su estado de vista. A continuación, puede recuperar el estado la próxima vez que se vea la carpeta. La manera preferida de guardar un estado de vista es llamar al [**método IShellBrowser::GetViewStateStream.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) Este método devuelve una [interfaz IStream](/windows/win32/api/objidl/nn-objidl-istream) que el objeto de vista de carpeta puede usar para guardar su estado. Al crear otra vista de carpeta, puede llamar al mismo método **IShellBrowser::GetViewStateStream** para obtener un puntero IStream que le permita leer la configuración guardada por las vistas de carpeta anteriores.

### <a name="translateacelerator"></a>TranslateAcelerator

Cuando el usuario presiona una tecla de método abreviado, Windows Explorer pasa el mensaje al objeto de vista de carpeta mediante una llamada a [**IShellView::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator). Devuelve S \_ FALSE para que Windows explorer procese el mensaje. Si el objeto de vista de carpeta ha procesado el mensaje, devuelva S \_ OK.

Cuando la ventana de vista de carpetas tiene el foco, Windows Explorer llama a [**IShellView::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) antes de que procese el mensaje. Dado que la mayoría de los mensajes normalmente están asociados Windows comandos de barra de menús o barra de herramientas del Explorador, el objeto de vista de carpeta normalmente debe devolver S \_ FALSE. Windows A continuación, el Explorador puede procesar el mensaje con normalidad. Devuelve S OK solo si el mensaje es específico de la carpeta y no desea que \_ Windows Explorer realice ningún procesamiento adicional. Si la vista de carpeta no tiene el foco, Windows Explorer procesa primero el mensaje. Llama a [**IShellBrowser::TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) solo si no controla el mensaje.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Uso de IShellBrowser para comunicarse con Windows Explorer

El objeto de vista de carpeta usa la interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) para comunicarse con Windows Explorer con diversos fines, entre los que se incluyen:

-   [Modificar la barra de menús Windows Explorer](#modifying-the-windows-explorer-menu-bar)
-   [Modificar la barra de herramientas Windows explorador](#modifying-the-windows-explorer-toolbar)
-   [Modificar la barra de estado Windows Explorer](#modifying-the-windows-explorer-status-bar)
-   [Almacenamiento de información específica de la vista](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Modificar la barra de menús Windows Explorer

La Windows de menús del Explorador de aplicaciones permite al usuario iniciar una variedad de comandos. De forma predeterminada, la barra de menús solo admite comandos específicos de Windows Explorer. Los mensajes [WM \_ COMMAND](../menurc/wm-command.md) relacionados se procesan mediante Windows Explorer y no se pasan al objeto de vista de carpeta. Sin embargo, puede modificar la barra de menús para incluir uno o varios elementos de menú específicos de la carpeta con [**IShellBrowser.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) Windows El Explorador pasa los mensajes WM COMMAND asociados de esos elementos al procedimiento de ventana del objeto \_ de carpeta para su procesamiento. También puede quitar o deshabilitar cualquier comando estándar que no se aplique a la aplicación.

Normalmente, los objetos de vista de carpeta modifican la barra de menús antes de que se muestre por primera vez la vista de carpeta. Deben devolver la barra de menús a su estado original cuando se destruye la vista de carpeta. Es posible que también tenga que modificar la barra de menús cada vez que la vista de carpeta aumenta o pierde el foco.

Dado Windows Explorer llama a [**IShellView::UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) cada vez que cambia el estado de la ventana de vista de carpetas, la modificación de la barra de menús normalmente se incluye en la implementación de ese método. El procedimiento básico para modificar la barra de menús Windows Explorer es:

1.  Llame [a CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) para crear un identificador de menú.
2.  Pase ese identificador de menú a Windows Explorer mediante una llamada [**a IShellBrowser::InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb). Windows El Explorador rellenará su información de menú.
3.  Modifique el menú según sea necesario.
4.  Llame [**a IShellBrowser::SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que Windows Explorer muestre la barra de menús modificada.

Windows El Explorador tiene seis menús emergentes en su barra de menús. Al igual que con todos los contenedores OLE, el menú Windows Explorer se divide en seis grupos: Archivo, Edición, Contenedor, Objeto, Ventana y Ayuda. En la tabla siguiente se enumeran Windows menús emergentes del Explorador de aplicaciones y su grupo asociado, junto con los iDs de menú.



| Menú emergente | id                     | Group (Grupo)     |
|-------------|------------------------|-----------|
| Archivo        | ARCHIVO DE MENÚ \_ DE FCIDM \_      | Archivo      |
| Editar        | EDICIÓN DEL MENÚ DE FCIDM \_ \_      | Archivo      |
| Ver        | VISTA DE MENÚ DE FCIDM \_ \_      | Contenedor |
| Favoritos   | FAVORITOS DEL MENÚ DE FCIDM \_ \_ | Contenedor |
| Herramientas       | HERRAMIENTAS DE MENÚ DE FCIDM \_ \_     | Contenedor |
| Ayuda        | AYUDA DEL MENÚ DE FCIDM \_ \_      | Periodo    |



 

Al pasar el identificador de menú a Windows Explorer mediante una llamada a [**IShellBrowser::InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb), también debe pasar un puntero a una estructura [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) cuyos miembros se han inicializado en cero.

Cuando [**IShellBrowser::InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) devuelve , Windows Explorer habrá agregado sus elementos de menú. A continuación, puede usar el identificador de menú devuelto con Windows funciones de menú estándar como [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para:

-   Agregue elementos a los Windows menús emergentes del Explorador de aplicaciones.
-   Modifique o elimine los elementos existentes en Windows menús emergentes del Explorador de aplicaciones.
-   Agregue nuevos menús emergentes.

Use los id. que aparecen en la tabla para identificar los distintos Windows menús emergentes del Explorador de aplicaciones.

> [!Note]  
> Para evitar conflictos con los Windows Explorer, los id. de los elementos de menú que agregue deben estar entre FCIDM \_ SHVIEWFIRST y FCIDM \_ SHVIEWLAST. Estos dos valores se definen en Shlobj.h.

 

Una vez que haya terminado de modificar el menú, llame a [**IShellBrowser::SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que Windows Explorer muestre la nueva barra de menús.

Una vez que se muestra inicialmente la vista de carpeta, Windows Explorer llama a [**IShellView::UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) cada vez que la vista de carpeta obtiene o pierde el foco. Si tiene elementos de menú que son sensibles al estado de la vista de carpeta, debe modificar el menú en consecuencia, cada vez que cambie el estado. Por ejemplo, es posible que tenga un elemento de menú que actúe sobre un elemento en la vista de carpeta seleccionada por el usuario. Debe deshabilitar o quitar este elemento de menú cuando la vista de carpeta pierda el foco.

Cuando Windows Explorer llama a [**IShellView::UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) para indicar que se está desactivando la vista de carpeta, restaure la barra de menús a su estado original mediante una llamada a [**IShellBrowser::RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb).

### <a name="modifying-the-windows-explorer-toolbar"></a>Modificar la barra de herramientas Windows explorer

Además de modificar la barra de menús Windows Explorer, también puede agregar botones a la barra de herramientas. Al igual que con la barra de menús, la modificación de la barra de herramientas suele formar parte de [**la implementación de IShellView::UIActivate.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) El procedimiento para agregar botones a la barra de herramientas Windows explorer es:

1.  Agregue el mapa de bits del botón a la lista de imágenes de la barra de herramientas.
2.  Defina la cadena de texto del botón.
3.  Agregue el botón a la barra de herramientas.

Para agregar un mapa de bits a la lista de imágenes de una barra de herramientas, envíe a la barra de herramientas un mensaje [ \_ ADDBITMAP](../controls/tb-addbitmap.md) de TB llamando a [**IShellBrowser::SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg). Para especificar el control de barra de herramientas, establezca el parámetro id del *método* en **FCW \_ TOOLBAR**. Establezca *wParam en el* número de imágenes de botón en el mapa de bits y *lParam* en la dirección de una [estructura TBADDBITMAP.](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) El índice de imagen se devuelve en el *parámetro pret.*

Hay dos maneras de definir una cadena para el botón:

-   Asigne la cadena al miembro **iString** de la estructura [TBBUTTON del](/windows/win32/api/commctrl/ns-commctrl-tbbutton) botón.
-   Llame [**a IShellBrowser::SendControlMsg para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) enviar al control de barra de herramientas un mensaje [ \_ ADDSTRING de TB.](../controls/tb-addstring.md) El *parámetro wParam* debe establecerse en cero y el *parámetro lParam* en la cadena. El índice de cadena se devuelve en el *parámetro pret.*

Para agregar el botón a la barra de herramientas, rellene una estructura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) y pásalo a [**IShellBrowser::SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Al igual que con el menú, el identificador de comando debe estar entre FCIDM \_ SHVIEWFIRST y \_ FCIDM SHVIEWLAST. A continuación, la barra de herramientas anexará el botón a la derecha de los botones existentes.

Por ejemplo, el siguiente fragmento de código agrega un botón estándar a la barra de herramientas Windows Explorer con un identificador de comando de IDB \_ MYBUTTON.


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



Para obtener más información sobre cómo controlar los controles de la barra de herramientas, vea [Controles de barra de herramientas](../controls/toolbar-control-reference.md).

### <a name="modifying-the-windows-explorer-status-bar"></a>Modificar la barra de estado Windows Explorer

Puede usar la barra de Windows explorer para mostrar una variedad de información útil. Hay dos maneras de usar la barra de estado:

-   Use [**IShellBrowser::SetStatusTextSB para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) mostrar una cadena de texto en la barra de estado.
-   Envíe mensajes directamente al control de barra de estado [**con IShellBrowser::SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

El primer método es sencillo, pero suficiente para muchos propósitos. Para mayor flexibilidad, puede enviar mensajes directamente al control de barra de estado llamando a [**IShellBrowser::SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) con el parámetro *id* establecido en **FCW \_ STATUS**. Para obtener más información sobre los controles de la barra de estado, vea [Barras de estado.](../controls/status-bars.md)

### <a name="storing-view-specific-information"></a>Almacenamiento de información específica de la vista

Cuando una vista está a punto de destruirse, a menudo resulta útil almacenar información como el estado o la configuración de la vista. Windows El Explorador le pide que realice esta tarea mediante una llamada [**a IShellView::SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate). La manera preferida de guardar información específica de la vista es llamar a [**IShellBrowser::GetViewStateStream.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) Este método proporciona una interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) que puede usar para almacenar la información. Puede usar cualquier formato de datos adecuado.

 

 
