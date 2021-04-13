---
title: Implementación de una vista de carpetas
description: Windows Shell proporciona una implementación predeterminada de la vista de carpetas, suele conocida como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- objeto de vista de carpeta
- IShellView
- IShellBrowser, objetos de vista de carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/11/2020
ms.locfileid: "104421558"
---
# <a name="implementing-a-folder-view"></a>Implementación de una vista de carpetas

Windows Shell proporciona una implementación predeterminada de la vista de carpetas, suele conocida como DefView, para que pueda evitar gran parte del trabajo de implementar su propia extensión de espacio de nombres. Dado que algunas características de vista no se pueden lograr mediante vistas personalizadas, a menudo se recomienda usar el objeto de vista de carpeta del sistema predeterminado en lugar de una vista personalizada. Para obtener más información, vea [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). En el resto de este tema se describe la implementación de una vista de carpeta personalizada que no admite las características de vista más recientes.

A diferencia de la vista de árbol, el explorador de Windows no administra el contenido de una vista de carpeta. En su lugar, la ventana vista de carpetas hospeda una ventana secundaria proporcionada por el objeto de carpeta. El objeto de carpeta es responsable de crear un objeto de vista de carpeta para mostrar el contenido de la carpeta en la ventana secundaria.

La clave para implementar un objeto de vista de carpeta es la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . El explorador de Windows usa esta interfaz para comunicarse con el objeto de vista de carpeta. Antes de mostrar una vista de carpeta, el explorador de Windows llama al método [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) del objeto de carpeta con *RIID* establecido en IID \_ IShellView. Cree un objeto de vista de carpeta y devuelva su interfaz **IShellView** . A continuación, el objeto de vista de carpeta debe crear una ventana secundaria de la ventana de vista de carpetas y usar la ventana secundaria para mostrar información sobre el contenido de la carpeta.

Además de controlar el modo en que se muestran los datos, las extensiones también pueden personalizar varias características del explorador de Windows. Por ejemplo, una extensión puede agregar elementos a la barra de herramientas o a la barra de menús, o Mostrar información en la barra de estado.

-   [Objeto de vista de carpeta](#the-folder-view-object)
-   [Inicializar el objeto de vista de carpeta](#initializing-the-folder-view-object)
-   [Mostrar la vista de carpetas](#displaying-the-folder-view)
-   [Implementación de IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [Actualizar](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [Uso de IShellBrowser para comunicarse con el explorador de Windows](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Modificar la barra de menús del explorador de Windows](#modifying-the-windows-explorer-menu-bar)
    -   [Modificar la barra de herramientas del explorador de Windows](#modifying-the-windows-explorer-toolbar)
    -   [Modificar la barra de estado del explorador de Windows](#modifying-the-windows-explorer-status-bar)
    -   [Almacenar información específica de la vista](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>Objeto de vista de carpeta

Un objeto de vista de carpeta es un objeto de modelo de objetos componentes (COM) que expone una interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Este objeto es responsable de:

-   Crear una ventana secundaria de la ventana vista de carpetas y utilizarla para mostrar el contenido de la carpeta.
-   Controlar la comunicación con el explorador de Windows.
-   Agregar comandos específicos de la carpeta a la barra de menús y la barra de herramientas del explorador de Windows y controlar esos comandos cuando se seleccionan.
-   Administrar la interacción del usuario con la ventana vista de carpetas, como mostrar menús contextuales o controlar las operaciones de arrastrar y colocar.

En este documento se describen los tres primeros temas. Dado que la interacción del usuario con la vista de carpetas tiene lugar dentro de la ventana secundaria, el objeto de vista de carpeta es responsable de controlarlo como lo haría con cualquier otra ventana.

El explorador de Windows solicita un objeto de vista de carpeta mediante una llamada a la [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) del objeto de carpeta con el valor de *RIID* establecido en IID \_ IShellView. El procedimiento para crear una vista de carpeta es:

1.  El objeto de carpeta crea una nueva instancia del objeto de vista de carpeta y devuelve un puntero a su interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) .
2.  El explorador de Windows inicializa el objeto de vista de carpeta mediante una llamada al método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Cree una ventana secundaria de la ventana vista de carpetas y devuelva su identificador al explorador de Windows.
3.  El objeto vista de carpeta usa la interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) del explorador de Windows para personalizar la barra de herramientas del explorador de Windows, la barra de menús y la barra de estado.
4.  El objeto de vista de carpeta muestra el contenido de la carpeta en la ventana secundaria.
5.  El objeto de vista de carpeta controla la interacción del usuario con la vista de carpetas y cualquier barra de herramientas o elemento de barra de menús específico de la carpeta.

## <a name="initializing-the-folder-view-object"></a>Inicializar el objeto de vista de carpeta

El explorador de Windows inicializa el objeto de vista de carpeta mediante una llamada al método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Los parámetros del método proporcionan el objeto de vista de carpeta con la información que necesita para crear la ventana secundaria que se usará para mostrar el contenido de la carpeta:

-   Puntero a la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) del objeto de vista de carpeta anterior. Este parámetro se puede establecer en **null**.
-   Estructura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) que contiene la configuración de la vista de carpeta anterior.
-   Puntero a la interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) del explorador de Windows.
-   Estructura [Rect](/previous-versions//ms536136(v=vs.85)) con las dimensiones de la ventana de vista de carpetas.

Se llama al método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) antes de que se destruya el objeto anterior de la vista de carpeta. Así, el puntero de la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) permite comunicarse con el objeto anterior de la vista de carpetas. Esta interfaz es principalmente útil si la carpeta anterior pertenecía a la extensión y utilizó el mismo esquema de presentación. Si es así, puede comunicarse con el objeto de vista de carpeta anterior para tales propósitos como intercambiar la configuración privada.

Una manera sencilla de determinar si el puntero [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) pertenece a la extensión es que todos los objetos de vista de carpeta expongan una interfaz privada. Llame a [IShellView:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar la interfaz privada y examine el valor devuelto para determinar si el objeto de vista de carpeta es uno de los suyos. Después, puede usar un método privado en esa interfaz para intercambiar información.

La estructura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) contiene la configuración de pantalla de la vista de carpeta anterior. La configuración principal es el modo de visualización: icono grande, icono pequeño, lista o detalles. También hay una marca que contiene los valores de una variedad de opciones de presentación, por ejemplo, si la vista debe alinearse a la izquierda. La visualización de la carpeta debe seguir estos valores en la medida de lo posible, para ofrecer a los usuarios una experiencia coherente a medida que pasan de una carpeta a otra. Debe almacenar esta estructura y actualizarla con el cambio de configuración. El explorador de Windows llama a [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) para obtener el valor más reciente de esta estructura antes de abrir la siguiente vista de carpeta.

La interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) se expone mediante el explorador de Windows. Esta interfaz es un complemento de [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) y permite que un objeto de vista de carpeta se comunique con el explorador de Windows. No hay ninguna otra manera de recuperar este puntero de interfaz, por lo que el objeto de vista de carpeta debe almacenarlo para su uso posterior. En concreto, debe llamar a [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para recuperar la ventana de la vista de carpeta primaria que usará para crear la ventana secundaria. Tenga en cuenta que el método IShellBrowser:: GetWindow no se incluye en la documentación de **IShellBrowser** porque se hereda de [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow). Después de almacenar el puntero de interfaz, recuerde llamar a [IShellBrowser:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento de referencias de la interfaz. Cuando ya no necesite la interfaz, llame a [IShellBrowser:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

Para crear la ventana secundaria:

1.  Examine las estructuras [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) y [Rect](/previous-versions//ms536136(v=vs.85)) .
2.  Si es necesario, obtenga la configuración privada del objeto de vista de carpeta anterior.
3.  Llame a [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para recuperar la ventana de la vista de carpeta primaria.
4.  Cree un elemento secundario de la ventana vista de carpetas obtenida en el paso anterior y vuelva al explorador de Windows.

## <a name="displaying-the-folder-view"></a>Mostrar la vista de carpetas

Después de crear la ventana secundaria y devolverla al explorador de Windows, puede mostrar el contenido de la carpeta. Normalmente, las extensiones muestran su información haciendo que la ventana secundaria hospede un [control de vista de lista](../controls/list-view-control-reference.md) o un **control WebBrowser**. El control de vista de lista le permite replicar la [vista clásica](web-view.md)del explorador de Windows. El control WebBrowser permite usar un documento HTML dinámico (DHTML) para mostrar la información, de forma similar a la vista Web del explorador de Windows. Para obtener más información, consulte la documentación de esos controles.

La ventana vista de carpetas siempre existe, incluso si no tiene el foco. Por lo tanto, debe mantener tres Estados para la ventana secundaria:

-   Activado con el foco. La vista de carpetas se ha creado y tiene el foco. Establezca los elementos de la barra de menús o de la barra de herramientas adecuados para un estado enfocado.
-   Activado sin foco. La vista de carpetas se ha creado y está activa, pero no tiene el foco. Establezca los elementos de la barra de menús o de la barra de herramientas adecuados para un estado sin foco. Omitir los elementos que se aplican a la selección de elementos en la vista de carpeta.
-   Desactivado. La vista de carpetas está a punto de ser destruida. Quitar todos los elementos de menú específicos de la carpeta.

El explorador de Windows notifica al objeto de vista de carpetas cuándo cambia el estado de la ventana mediante una llamada a [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate). A su vez, el objeto de vista de carpeta debe notificar al explorador de Windows cuando un usuario activa la ventana de vista de carpetas mediante una llamada a [**IShellBrowser:: OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive). Para obtener más información sobre esta interfaz, consulte [uso de IShellBrowser para comunicarse con el explorador de Windows](#using-ishellbrowser-to-communicate-with-windows-explorer).

Mientras la vista de la carpeta está activa, debe procesar los mensajes de Windows, como [el \_ tamaño de WM](../winmsg/wm-size.md), que pertenecen a la ventana secundaria. El procedimiento de ventana también recibirá mensajes de [ \_ comandos de WM](../menurc/wm-command.md) para cualquier elemento que se haya agregado a la barra de menús o la barra de herramientas del explorador de Windows.

Después de crear la vista de carpetas, el explorador de Windows llama a la interfaz [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) del objeto de vista de carpeta para pasarle una gran variedad de información. El objeto debe modificar su presentación en consecuencia. Cuando la vista de carpetas está a punto de ser destruida, el explorador de Windows notifica el objeto de vista de carpeta mediante una llamada a su método [**IShellView::D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) .

## <a name="implementing-ishellview"></a>Implementación de IShellView

Una vez creado el objeto de carpeta, el explorador de Windows llama a varios métodos [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) para solicitar información o notificar a un objeto de un cambio en el estado del explorador de Windows. En esta sección se describe cómo implementar esos métodos **IShellView** . Los métodos restantes se usan para fines más especializados, como el cuadro de diálogo Abrir archivo común. Para obtener más información, consulte la documentación de **IShellView** .

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

Cuando un usuario selecciona **Opciones de carpeta** en el menú **herramientas** del explorador de Windows, se muestra una hoja de propiedades que permite al usuario modificar las opciones de carpeta. El explorador de Windows llama al método [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) del objeto de vista de carpeta para que pueda agregar una página a esta hoja de propiedades.

El explorador de Windows pasa un puntero a una función de devolución de llamada [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) en el parámetro *lpfn* de [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Llame a [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) para crear la página y, a continuación, llame a AddPropSheetPageProc para agregarla a la hoja de propiedades. Para obtener más información sobre cómo controlar las hojas de propiedades, vea [hojas de propiedades](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>GetCurrentInfo

Cuando el usuario cambia de una carpeta a otra, el explorador de Windows intenta mantener una vista de carpeta similar. Por ejemplo, si la vista de carpeta anterior mostró iconos grandes, el siguiente también debe ser. Cuando el explorador de Windows llama a [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) para inicializar el objeto de vista de carpeta, el método recibe una estructura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Esta estructura contiene información que le permite hacer que la vista de carpetas sea coherente con la vista de carpeta anterior.

Para asegurarse de que la vista siguiente sea coherente con la vista actual, almacene la estructura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Si la vista cambia, por ejemplo, de iconos grandes a pequeños, actualice la estructura en consecuencia. Antes de cambiar de vista, el explorador de Windows llamará a [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) para solicitar los valores de **FOLDERSETTINGS** actuales para pasarlos al siguiente objeto de vista de carpeta.

### <a name="refresh"></a>Actualizar

El usuario puede asegurarse de que la vista de carpetas refleja el estado actual de la carpeta seleccionando **Actualizar** en el menú **Ver** o presionando la tecla F5. Cuando el usuario lo hace, el explorador de Windows llama al método [**IShellView:: Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) . El objeto de vista de carpeta debe actualizar inmediatamente la presentación de la vista de carpetas.

### <a name="saveviewstate"></a>SaveViewState

El explorador de Windows llama al método [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) para solicitar al objeto de vista de carpeta que guarde su estado de vista. Después, puede recuperar el estado la próxima vez que se vea la carpeta. La mejor manera de guardar el estado de vista es llamando al método [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) . Este método devuelve una interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) que el objeto de vista de carpetas puede usar para guardar su estado. Al crear otra vista de carpetas, puede llamar al mismo método **IShellBrowser:: GetViewStateStream** para obtener un puntero IStream que le permita leer la configuración guardada por vistas de carpeta anteriores.

### <a name="translateacelerator"></a>TranslateAcelerator

Cuando el usuario presiona una tecla de método abreviado, el explorador de Windows pasa el mensaje al objeto de vista de carpeta mediante una llamada a [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator). Devuelve S \_ false para que el explorador de Windows procese el mensaje. Si el objeto de vista de carpeta ha procesado el mensaje, devuelva el valor \_ correcto.

Cuando la ventana vista de carpetas tiene el foco, el explorador de Windows llama a [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) antes de procesar el mensaje. Dado que la mayoría de los mensajes están asociados normalmente con los comandos de barra de menús o barra de herramientas del explorador de Windows, el objeto de vista de carpeta normalmente debería devolver S \_ false. Después, el explorador de Windows puede procesar el mensaje con normalidad. Devuelve S \_ OK solo si el mensaje es específico de la carpeta y no desea que el explorador de Windows realice ningún procesamiento adicional. Si la vista de la carpeta no tiene el foco, el explorador de Windows procesa el mensaje en primer lugar. Solo llama a [**IShellBrowser:: TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) si no controla el mensaje.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Uso de IShellBrowser para comunicarse con el explorador de Windows

El objeto de vista de carpeta usa la interfaz [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) para comunicarse con el explorador de Windows para una variedad de propósitos, entre los que se incluyen:

-   [Modificar la barra de menús del explorador de Windows](#modifying-the-windows-explorer-menu-bar)
-   [Modificar la barra de herramientas del explorador de Windows](#modifying-the-windows-explorer-toolbar)
-   [Modificar la barra de estado del explorador de Windows](#modifying-the-windows-explorer-status-bar)
-   [Almacenar información específica de la vista](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Modificar la barra de menús del explorador de Windows

La barra de menús del explorador de Windows permite al usuario iniciar diversos comandos. De forma predeterminada, la barra de menús solo admite comandos que son específicos del explorador de Windows. El explorador de Windows procesa los mensajes de [ \_ comando de WM](../menurc/wm-command.md) relacionados y no se pasan al objeto de vista de carpeta. Sin embargo, puede modificar la barra de menús para incluir uno o varios elementos de menú específicos de la carpeta con [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser). El explorador de Windows pasa los \_ mensajes de comando de WM asociados de esos elementos al procedimiento de ventana del objeto de carpeta para su procesamiento. También puede quitar o deshabilitar los comandos estándar que no se aplican a la aplicación.

Los objetos de vista de carpeta normalmente modifican la barra de menús antes de que se muestre la vista de carpetas por primera vez. Deben devolver la barra de menús a su estado original cuando se destruya la vista de carpetas. Es posible que también tenga que modificar la barra de menús cada vez que la vista de carpetas gane o pierda el foco.

Dado que el explorador de Windows llama a [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) cada vez que cambia el estado de la ventana de vista de carpeta, la modificación de la barra de menús se incluye normalmente en la implementación de ese método. El procedimiento básico para modificar la barra de menús del explorador de Windows es:

1.  Llame a [CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) para crear un identificador de menú.
2.  Pase ese identificador de menú al explorador de Windows mediante una llamada a [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb). El explorador de Windows rellenará la información del menú.
3.  Modifique el menú según sea necesario.
4.  Llame a [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que el explorador de Windows muestre la barra de menús modificada.

El explorador de Windows tiene seis menús emergentes en la barra de menús. Al igual que con todos los contenedores OLE, el menú del explorador de Windows se divide en seis grupos: archivo, edición, contenedor, objeto, ventana y ayuda. En la tabla siguiente se enumeran los menús emergentes del explorador de Windows y su grupo asociado, junto con los identificadores de menú.



| Menú emergente | id                     | Grupo     |
|-------------|------------------------|-----------|
| Archivo        | \_archivo de menú FCIDM \_      | Archivo      |
| Editar        | \_edición del menú FCIDM \_      | Archivo      |
| Ver        | \_vista de menú FCIDM \_      | Contenedor |
| Favoritos   | \_favoritos del menú FCIDM \_ | Contenedor |
| Herramientas       | \_herramientas de menú FCIDM \_     | Contenedor |
| Ayuda        | \_ayuda del menú FCIDM \_      | Periodo    |



 

Al pasar el identificador de menú al explorador de Windows mediante una llamada a [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb), también debe pasar un puntero a una estructura [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) cuyos miembros se hayan inicializado en cero.

Cuando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) devuelve, el explorador de Windows habrá agregado sus elementos de menú. Después, puede usar el identificador de menú devuelto con las funciones de menú estándar de Windows, como [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) :

-   Agregar elementos a los menús emergentes del explorador de Windows.
-   Modificar o eliminar elementos existentes en los menús emergentes del explorador de Windows.
-   Agregar nuevos menús emergentes.

Use los identificadores enumerados en la tabla para identificar los distintos menús emergentes del explorador de Windows.

> [!Note]  
> Para evitar conflictos con los identificadores de comando del explorador de Windows, los identificadores de los elementos de menú que agregue deben estar entre FCIDM \_ SHVIEWFIRST y FCIDM \_ SHVIEWLAST. Estos dos valores se definen en ShlObj. h.

 

Cuando haya terminado de modificar el menú, llame a [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que el explorador de Windows muestre la nueva barra de menús.

Después de mostrar inicialmente la vista de carpetas, el explorador de Windows llama a [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) cada vez que la vista de carpeta gana o pierde el foco. Si tiene algún elemento de menú que sea sensible al estado de la vista de la carpeta, debe modificar el menú en consecuencia, cada vez que cambie el estado. Por ejemplo, podría tener un elemento de menú que actúe en un elemento de la vista de carpetas seleccionado por el usuario. Debe deshabilitar o quitar este elemento de menú cuando la vista de carpetas pierda el foco.

Cuando el explorador de Windows llama a [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) para indicar que la vista de carpetas se está desactivando, restaure la barra de menús a su estado original llamando a [**IShellBrowser:: RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb).

### <a name="modifying-the-windows-explorer-toolbar"></a>Modificar la barra de herramientas del explorador de Windows

Además de modificar la barra de menús del explorador de Windows, también puede agregar botones a la barra de herramientas. Al igual que con la barra de menús, la modificación de la barra de herramientas suele ser parte de la implementación [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) . El procedimiento para agregar botones a la barra de herramientas del explorador de Windows es:

1.  Agregue el mapa de bits del botón a la lista de imágenes de la barra de herramientas.
2.  Defina la cadena de texto del botón.
3.  Agregue el botón a la barra de herramientas.

Para agregar un mapa de bits a la lista de imágenes de una barra de herramientas, envíe la barra de herramientas a un mensaje de [TB \_ ADDBITMAP](../controls/tb-addbitmap.md) llamando a [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg). Para especificar el control de barra de herramientas, establezca el parámetro *ID* del método en la **barra de \_ herramientas FCW**. Establezca *wParam* en el número de imágenes de botón en el mapa de bits y *lParam* en la dirección de una estructura [TBADDBITMAP](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) . El índice de la imagen se devuelve en el parámetro *pret* .

Hay dos maneras de definir una cadena para el botón:

-   Asigne la cadena al miembro **iString** de la estructura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) del botón.
-   Llame a [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) para enviar el control de la barra de herramientas a un mensaje de [TB \_ ADDSTRING](../controls/tb-addstring.md) . El parámetro *wParam* debe establecerse en cero y el parámetro *lParam* en la cadena. El índice de cadena se devuelve en el parámetro *pret* .

Para agregar el botón a la barra de herramientas, rellene una estructura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) y pásela a [**IShellBrowser:: SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Como con el menú, el identificador de comando debe estar entre FCIDM \_ SHVIEWFIRST y FCIDM \_ SHVIEWLAST. A continuación, la barra de herramientas anexará el botón a la derecha de los botones existentes.

Por ejemplo, el siguiente fragmento de código agrega un botón estándar a la barra de herramientas del explorador de Windows con un ID. de comando de IDB \_ MyButton.


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



Para obtener más información sobre cómo controlar los controles de la barra de herramientas, vea [controles de barra de herramientas](../controls/toolbar-control-reference.md).

### <a name="modifying-the-windows-explorer-status-bar"></a>Modificar la barra de estado del explorador de Windows

Puede usar la barra de estado del explorador de Windows para mostrar una gran variedad de información útil. Hay dos maneras de usar la barra de estado:

-   Use [**IShellBrowser:: SetStatusTextSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) para mostrar una cadena de texto en la barra de estado.
-   Enviar mensajes directamente al control de barra de estado con [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

El primer método es sencillo, pero suficiente para muchos propósitos. Para mayor flexibilidad, puede enviar mensajes directamente al control de la barra de estado mediante una llamada a [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) con el parámetro *ID* establecido en **FCW \_ status**. Para obtener más información sobre los controles de barra de estado, vea [barras de estado](../controls/status-bars.md).

### <a name="storing-view-specific-information"></a>Almacenar información específica de la vista

Cuando una vista está a punto de ser destruida, a menudo resulta útil almacenar información como el estado o la configuración de la vista. El explorador de Windows le pide que realice esta tarea mediante una llamada a [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate). La mejor manera de guardar la información específica de la vista es llamar a [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream). Este método proporciona una interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) que puede usar para almacenar la información. Puede usar cualquier formato de datos adecuado.

 

 
