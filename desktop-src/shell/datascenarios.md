---
description: Este documento presenta escenarios comunes de transferencia de datos de Shell y describe cómo implementar cada uno de ellos en la aplicación.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Control de escenarios de transferencia de datos de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35855b66e4108580d5bac305855837563ca59785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984318"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Control de escenarios de transferencia de datos de shell

En el documento de [objeto de datos de Shell](dataobject.md) se describe el enfoque general que se usa para transferir datos de Shell con arrastrar y colocar o el portapapeles. Sin embargo, para implementar la transferencia de datos de Shell en la aplicación, también debe comprender cómo aplicar estos principios y técnicas generales a las diversas formas en que se pueden transferir los datos de Shell. Este documento presenta escenarios comunes de transferencia de datos de Shell y describe cómo implementar cada uno de ellos en la aplicación.

-   [Directrices generales](#general-guidelines)
-   [Copiar nombres de archivo del portapapeles en una aplicación](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Extraer los nombres de archivo del objeto de datos](#extracting-the-file-names-from-the-data-object)
-   [Copiar el contenido de un archivo colocado en una aplicación](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Usar el \_ formato CFSTR FILECONTENTS para extraer datos de un archivo](/windows)
-   [Control de operaciones de movimiento optimizadas](#handling-optimized-move-operations)
-   [Control de operaciones de eliminación y pegado](#handling-delete-on-paste-operations)
-   [Transferencia de datos hacia y desde carpetas virtuales](#transfering-data-to-and-from-virtual-folders)
    -   [Aceptar datos de una carpeta virtual](#accepting-data-from-a-virtual-folder)
    -   [Transferir datos hacia y desde una extensión de espacio de nombres](#transferring-data-to-and-from-a-namespace-extension)
-   [Quitar archivos de la papelera de reciclaje](#dropping-files-on-the-recycle-bin)
-   [Crear e importar archivos de rechazo](#creating-and-importing-scrap-files)
    -   [Compatibilidad con acciones de ida y vuelta](#round-trip-support)
    -   [Formatos de datos almacenados en caché](#cached-data-formats)
    -   [Representación diferida](#delayed-rendering)
-   [Arrastrar y colocar objetos de Shell de forma asincrónica](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Usar IASyncOperation/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Aunque cada uno de estos escenarios trata una operación de transferencia de datos específica, muchas de ellas se aplican a una serie de escenarios relacionados. Por ejemplo, la principal diferencia entre la mayoría de las transferencias de Portapapeles y de arrastrar y colocar es el modo en que el objeto de datos llega al destino. Una vez que el destino tiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, los procedimientos para extraer información son en gran medida los mismos para ambos tipos de transferencia de datos. Sin embargo, algunos de los escenarios se limitan a un tipo de operación específico. Consulte el escenario individual para obtener más información.

 

## <a name="general-guidelines"></a>Instrucciones generales

En cada una de las secciones siguientes se describe un escenario de transferencia de datos único y bastante específico. Sin embargo, las transferencias de datos suelen ser más complejas y pueden implicar aspectos de varios escenarios. Por lo general, no sabe de antemano qué escenario necesitará controlar. Estas son algunas directrices generales que se deben tener en cuenta.

Para orígenes de datos:

-   Los formatos del portapapeles de Shell, con la excepción de [CF \_ HDROP](clipboard.md), no están predefinidos. Cada formato que desee usar debe registrarse mediante una llamada a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Los formatos de los objetos de datos se proporcionan en el orden de preferencia del origen. Enumere el objeto de datos y elija el primero que puede consumir.
-   Incluya tantos formatos como pueda admitir. Por lo general, no sabe dónde se quitará el objeto de datos. Esta práctica mejora la probabilidad de que el objeto de datos contenga un formato que pueda aceptar el destino de colocación.
-   Los archivos existentes se deben ofrecer con el formato [ \_ HDROP de CF](clipboard.md) .
-   Ofrezca datos similares a los archivos con formatos de [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md) . Este enfoque permite al destino crear un archivo a partir de un objeto de datos sin necesidad de saber nada sobre el almacenamiento de datos subyacente. Normalmente debería presentar los datos como una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Este mecanismo de transferencia de datos es más flexible que un objeto de memoria global y utiliza mucha menos memoria.
-   Los orígenes de arrastre deben ofrecer el formato [CFSTR \_ SHELLIDLIST](clipboard.md) al arrastrar elementos de Shell. Los objetos de datos de los elementos se pueden adquirir a través de los métodos [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) o [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) . Los orígenes de datos pueden crear una implementación de objeto de datos estándar que admita el formato [ \_ SHELLIDLIST de CFSTR](clipboard.md) con [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject).
-   Los destinos de colocación que deseen saber sobre los elementos que se arrastran mediante el modelo de programación de elementos de Shell pueden convertir un objeto IDataObject en un [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) con [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).
-   Usar cursores de comentarios estándar.
-   Compatibilidad con arrastrar a la izquierda y a la derecha.
-   Usar el propio objeto de datos a partir de un objeto incrustado. Este enfoque permite que la aplicación recupere cualquier formato adicional que tenga el objeto de datos para ofrecer y evitar la creación de una capa adicional de contención. Por ejemplo, un objeto incrustado del servidor A se arrastra desde el servidor o contenedor B y se coloca en el contenedor C. C debe crear un objeto incrustado del servidor A, no un objeto incrustado del servidor B que contiene un objeto incrustado del servidor A.
-   Recuerde que el shell podría usar las operaciones [de eliminación o eliminación](#handling-delete-on-paste-operations) [optimizadas](#handling-optimized-move-operations) al mover archivos. La aplicación debe ser capaz de reconocer estas operaciones y responder de forma adecuada.

Para destinos de datos:

-   Los formatos del portapapeles de Shell, con la excepción de [CF \_ HDROP](clipboard.md), no están predefinidos. Cada formato que desee usar debe registrarse mediante una llamada a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Implemente y registre un destino de colocación OLE. Evite el uso de destinos de Windows 3,1 o el mensaje de [**\_ DROPFILES de WM**](wm-dropfiles.md) , si es posible.
-   Los formatos contenidos en un objeto de datos varían en función de dónde proceda el objeto. Dado que generalmente no se sabe de antemano de dónde procede un objeto de datos, no suponga que un determinado formato estará presente. El objeto de datos debe enumerar los formatos en orden de calidad, empezando por el mejor. Por lo tanto, para obtener el mejor formato disponible, las aplicaciones suelen enumerar los formatos disponibles y usar el primer formato en la enumeración que pueden admitir.
-   Compatibilidad con la función de arrastrar hacia la derecha. Puede personalizar el menú contextual de arrastrar mediante la creación de un [controlador de arrastrar y colocar](context-menu-handlers.md).
-   Si la aplicación va a aceptar archivos existentes, debe ser capaz de controlar el [formato \_ HDROP de CF](clipboard.md) .
-   En general, las aplicaciones que aceptan archivos también deben administrar los formatos de [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md) . Aunque los archivos del sistema de archivos tienen el formato [CF \_ HDROP](clipboard.md) , los archivos de proveedores como las extensiones de espacio de nombres suelen usar [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md). Entre los ejemplos se incluyen carpetas Windows CE, carpetas de protocolo de transferencia de archivos (FTP), carpetas web y carpetas CAB. Normalmente, el origen implementa una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) para presentar los datos de su almacenamiento como un archivo.
-   Recuerde que el shell podría usar las operaciones [de eliminación o eliminación](#handling-delete-on-paste-operations) [optimizadas](#handling-optimized-move-operations) al mover archivos. La aplicación debe ser capaz de reconocer estas operaciones y responder de forma adecuada.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Copiar nombres de archivo del portapapeles en una aplicación

**Escenario:** Un usuario selecciona uno o varios archivos en el explorador de Windows y los copia en el portapapeles. La aplicación extrae los nombres de archivo y los pega en el documento.

Este escenario podría usarse, por ejemplo, para permitir que un usuario cree un vínculo HTML cortando y pegando el archivo en la aplicación. A continuación, la aplicación puede extraer el nombre de archivo del objeto de datos y procesarlo para crear una etiqueta delimitadora.

Cuando un usuario selecciona un archivo en el explorador de Windows y lo copia en el portapapeles, el shell crea un objeto de datos. A continuación, llama a [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) para colocar un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el portapapeles.

Cuando el usuario selecciona el comando **pegar** desde el menú o la barra de herramientas de la aplicación:

1.  Llame a [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) para recuperar la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
2.  Llame a [**IDataObject:: del EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) para solicitar un objeto de enumerador.
3.  Use la interfaz [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) del objeto de enumerador para enumerar los formatos contenidos en el objeto de datos.

> [!Note]  
> Los dos pasos finales de este procedimiento se incluyen por integridad. Normalmente no son necesarios para las transferencias de archivos simples. Todos los objetos de datos utilizados para este tipo de transferencia de datos deben contener el formato [CF \_ HDROP](clipboard.md) , que se puede utilizar para determinar los nombres de los archivos que contiene el objeto. Sin embargo, para las transferencias de datos más generales, debe enumerar los formatos y seleccionar el mejor que pueda controlar la aplicación.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Extraer los nombres de archivo del objeto de datos

El siguiente paso consiste en extraer uno o varios nombres de archivo del objeto de datos y pegarlos en la aplicación. Tenga en cuenta que el procedimiento descrito en esta sección para extraer un nombre de archivo de un objeto de datos se aplica igualmente bien a las transferencias de arrastrar y colocar.

La manera más sencilla de recuperar nombres de archivo de un objeto de datos es el formato [ \_ HDROP de CF](clipboard.md) :

1.  Llame a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Establezca el miembro **cfFormat** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en [CF \_ HDROP](clipboard.md) y el miembro **tymed** en [tymed \_ HGLOBAL](dataobject.md). El miembro **dwAspect** se establece normalmente en el \_ contenido de DVASPECT. Sin embargo, si necesita que la ruta de acceso del archivo tenga el formato corto (8,3), establezca **dwAspect** en DVASPECT \_ Short.

    Cuando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) devuelve, el miembro **hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) apunta a un objeto de memoria global que contiene los datos.

2.  Cree una variable HDROP y establézcala en el miembro **hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . La variable HDROP es ahora un identificador de una estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) , seguido de una cadena terminada en null que contiene las rutas de acceso de archivo completas de los archivos copiados.
3.  Determine el número de rutas de acceso de archivo que se encuentran en la lista mediante una llamada a [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) con el parámetro *IFile* establecido en 0xFFFFFFFF. La función devuelve el número de rutas de acceso de archivo de la lista. El índice de base cero de la ruta de acceso del archivo de esta lista se usa en el paso siguiente para identificar una ruta de acceso determinada.
4.  Extraiga las rutas de acceso de archivo del objeto de memoria global llamando a [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) una vez para cada archivo, con *iFile* establecido en el índice del archivo.
5.  Procese las rutas de acceso de archivo según sea necesario y péguelas en la aplicación.
6.  Llame a [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) y pase el puntero a la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que pasó a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) en el paso 1. Una vez que haya liberado la estructura, el valor de HDROP que ha creado en el paso 2 ya no es válido y no debe usarse.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Copiar el contenido de un archivo colocado en una aplicación

**Escenario:** Un usuario arrastra uno o más archivos desde el explorador de Windows y los coloca en la ventana de la aplicación. La aplicación extrae el contenido de los archivos y lo pega en la aplicación.

En este escenario se usa la función de arrastrar y colocar para transferir los archivos del explorador de Windows a la aplicación. Antes de la operación, la aplicación debe:

1.  Llame a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para registrar los formatos de Portapapeles de Shell necesarios.
2.  Llame a [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) para registrar una ventana de destino y la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la aplicación.

Una vez que el usuario inicia la operación seleccionando uno o varios archivos y empezando a arrastrarlos:

1.  El explorador de Windows crea un objeto de datos y carga en él los formatos admitidos.
2.  El explorador de Windows llama a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) para iniciar el bucle de arrastre.
3.  Cuando la imagen de arrastre llega a la ventana de destino, el sistema le notifica mediante una llamada a [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Para determinar qué contiene el objeto de datos, llame al método [**IDataObject:: del EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) del objeto de datos. Utilice el objeto de enumerador devuelto por el método para enumerar los formatos contenidos en el objeto de datos. Si la aplicación no desea aceptar ninguno de estos formatos, devuelva DROPEFFECT \_ ninguno. Para los fines de este escenario, la aplicación debe omitir cualquier objeto de datos que no contenga formatos usados para transferir archivos, como [CF \_ HDROP](clipboard.md).
5.  Cuando el usuario quita los datos, el sistema llama a [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).
6.  Use la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extraer el contenido de los archivos.

Hay varias maneras de extraer el contenido de un objeto de Shell de un objeto de datos. En general, use el orden siguiente:

-   Si el archivo contiene un formato de [ \_ texto CF](clipboard.md) , los datos son texto ANSI. Puede usar el formato de \_ texto CF para extraer los datos, en lugar de abrir el propio archivo.
-   Si el archivo contiene un objeto OLE vinculado o incrustado, el objeto de datos contiene un \_ formato EMBEDDEDOBJECT de CF. Utilice técnicas OLE estándar para extraer los datos. [Los archivos de rechazo](#creating-and-importing-scrap-files) siempre contienen un \_ formato CF EMBEDDEDOBJECT.
-   Si el objeto de Shell procede del sistema de archivos, el objeto de datos contiene un formato [CF \_ HDROP](clipboard.md) con los nombres de los archivos. Extraiga el nombre de archivo de [CF \_ HDROP](clipboard.md) y llame a [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) para crear un nuevo objeto vinculado o incrustado. Para obtener una explicación sobre cómo recuperar un nombre de archivo desde un formato de [CF \_ HDROP](clipboard.md) , vea [Copiar nombres de archivo del portapapeles en una aplicación](#copying-file-names-from-the-clipboard-to-an-application).
-   Si el objeto de datos contiene un formato de [CFSTR \_ FILEDESCRIPTOR](clipboard.md) , puede extraer el contenido de un archivo desde el formato de [CFSTR \_ FILECONTENTS](clipboard.md) del archivo. Para obtener una explicación de este procedimiento, vea [usar el \_ formato CFSTR FILECONTENTS para extraer datos de un archivo](/windows).
-   Antes de la [versión 4,71](versions.md)de Shell, una aplicación indicaba que se transfiriendo un tipo de archivo de acceso directo estableciendo **FD \_ LINKUI** en el miembro **dwFlags** de la estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . En el caso de las versiones posteriores del shell, la manera preferida de indicar que los métodos abreviados se están transfiriendo es usar el formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ Link. Este enfoque es mucho más eficaz que extraer la estructura **FILEDESCRIPTOR** solo para comprobar una marca.

Si el proceso de extracción de datos va a ser largo, es posible que desee realizar la operación de forma asincrónica en un subproceso en segundo plano. El subproceso principal puede continuar sin retrasos innecesarios. Para obtener información sobre cómo administrar la extracción de datos asincrónica, vea [arrastrar y colocar objetos de Shell de forma asincrónica](#dragging-and-dropping-shell-objects-asynchronously).

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Usar el \_ formato CFSTR FILECONTENTS para extraer datos de un archivo

El formato [CFSTR \_ FILECONTENTS](clipboard.md) proporciona una manera muy flexible y eficaz de transferir el contenido de un archivo. Ni siquiera es necesario almacenar los datos como un único archivo. Lo único que se necesita para este formato es que el objeto de datos presente los datos en el destino como si fuera un archivo. Por ejemplo, los datos reales pueden ser una sección de un documento de texto o un bloque de datos extraídos de una base de datos. El destino puede tratar los datos como un archivo y no necesita saber nada sobre el mecanismo de almacenamiento subyacente.

Las extensiones de espacio de nombres suelen usar [CFSTR \_ FILECONTENTS](clipboard.md) para transferir datos porque este formato no supone ningún mecanismo de almacenamiento concreto. Una extensión de espacio de nombres puede usar cualquier mecanismo de almacenamiento adecuado y usar este formato para presentar sus objetos a las aplicaciones como si fueran archivos.

El mecanismo de transferencia de datos para [CFSTR \_ FILECONTENTS](clipboard.md) suele ser [TYMED \_ ISTREAM](dataobject.md). La transferencia de un puntero de interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) requiere mucha menos memoria que cargar los datos en un objeto de memoria global, y **IStream** es una forma más sencilla de representar datos que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Un formato de [CFSTR \_ FILECONTENTS](clipboard.md) siempre va acompañado de un formato [CFSTR de \_ FILEDESCRIPTOR](clipboard.md) . Primero debe examinar el contenido de este formato. Si se transfiere más de un archivo, el objeto de datos contendrá realmente varios formatos de [CFSTR \_ FILECONTENTS](clipboard.md) , uno para cada archivo. El formato de [CFSTR \_ FILEDESCRIPTOR](clipboard.md) contiene el nombre y los atributos de cada archivo, y proporciona un valor de índice para cada archivo que se necesita para extraer el formato [CFSTR \_ FILECONTENTS](clipboard.md) de un archivo determinado.

Para extraer un formato de [CFSTR \_ FILECONTENTS](clipboard.md) :

1.  Extraiga el formato de [CFSTR \_ FILEDESCRIPTOR](clipboard.md) como valor [ \_ HGLOBAL de TYMED](dataobject.md) .
2.  El miembro **hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) devuelta apunta a un objeto de memoria global. Bloquee el objeto pasando el valor **hGlobal** a [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock).
3.  Convierta el puntero devuelto por [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) en un puntero [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) . Apuntará a una estructura **FILEGROUPDESCRIPTOR** seguida de una o más estructuras [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Cada estructura de **FILEDESCRIPTOR** contiene una descripción de un archivo que se encuentra en uno de los formatos de [CFSTR \_ FILECONTENTS](clipboard.md) que lo acompañan.
4.  Examine las estructuras [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para determinar cuál corresponde al archivo que desea extraer. El índice de base cero de esa estructura **FILEDESCRIPTOR** se usa para identificar el formato de [ \_ FILECONTENTS de CFSTR](clipboard.md) del archivo. Dado que el tamaño de un bloque de memoria global no es preciso para bytes, utilice los miembros **nFileSizeLow** y **nFileSizeHigh** de la estructura para determinar cuántos bytes representan el archivo en el objeto de memoria global.
5.  Llame a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con el miembro **cfFormat** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) establecido en el valor [CFSTR \_ FILECONTENTS](clipboard.md) y el miembro **lIndex** establecido en el índice que determinó en el paso anterior. Normalmente, el miembro **tymed** se establece en [tymed \_ HGLOBAL](dataobject.md) \| tymed \_ ISTREAM \| tymed \_ ISTORAGE. Después, el objeto de datos puede elegir su mecanismo de transferencia de datos preferido.
6.  La estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que devuelve [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) contendrá un puntero a los datos del archivo. Examine el miembro **tymed** de la estructura para determinar el mecanismo de transferencia de datos.
7.  Si **tymed** se establece en [TYMED \_ ISTREAM](dataobject.md) o tymed \_ ISTORAGE, use la interfaz para extraer los datos. Si **tymed** se establece en tymed \_ HGLOBAL, los datos se incluyen en un objeto de memoria global. Para obtener una explicación sobre cómo extraer datos de un objeto de memoria global, consulte la sección *extraer un objeto de memoria global de un objeto de datos* del [objeto de datos de Shell](dataobject.md).
8.  Llame a [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) para desbloquear el objeto de memoria global que bloqueó en el paso 2.

## <a name="handling-optimized-move-operations"></a>Control de operaciones de movimiento optimizadas

**Escenario:** Un archivo se mueve del sistema de archivos a una extensión de espacio de nombres mediante un movimiento optimizado.

En una operación de movimiento convencional, el destino realiza una copia de los datos y el origen elimina el original. Este procedimiento puede ser ineficaz porque requiere dos copias de los datos. Con objetos grandes como bases de datos, es posible que una operación de movimiento convencional no sea práctica.

Con un movimiento optimizado, el destino utiliza su conocimiento sobre cómo se almacenan los datos para controlar toda la operación de movimiento. Nunca hay una segunda copia de los datos y no es necesario que el origen elimine los datos originales. Los datos de Shell se adaptan bien a los movimientos optimizados porque el destino puede controlar toda la operación mediante la API de Shell. Un ejemplo típico es mover archivos. Una vez que el destino tiene la ruta de acceso de un archivo que se va a trasladar, puede usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para moverlo. No es necesario que el origen elimine el archivo original.

> [!Note]  
> Normalmente, el shell usa un movimiento optimizado para migrar archivos. Para controlar correctamente la transferencia de datos de Shell, la aplicación debe ser capaz de detectar y administrar un movimiento optimizado.

 

Los movimientos optimizados se controlan de la siguiente manera:

1.  El origen llama a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) con el parámetro *DWEFFECT* establecido en DROPEFFECT \_ Move para indicar que los objetos de origen se pueden trasladar.
2.  El destino recibe el \_ valor de movimiento DROPEFFECT a través de uno de sus métodos [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) , lo que indica que se permite un movimiento.
3.  El destino copia el objeto (movimiento no optimizado) o mueve el objeto (movimiento optimizado).
4.  A continuación, el destino indica al origen si es necesario eliminar los datos originales.

    Un movimiento optimizado es la operación predeterminada, con los datos eliminados por el destino. Para informar al origen de que se ha realizado un movimiento optimizado:

    -   -   El destino establece el valor de *pdwEffect* recibido a través de su método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) en un valor distinto de DROPEFFECT \_ Move. Normalmente se establece en DROPEFFECT \_ None o DROPEFFECT \_ Copy. El valor se devolverá al origen mediante [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   El destino también llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos y le pasa un identificador de formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ None. Esta llamada al método es necesaria porque es posible que algunos destinos de colocación no establezcan correctamente el parámetro *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . El formato de [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) es el método confiable para indicar que ha tenido lugar un movimiento optimizado.

    Si el destino ha realizado un movimiento no optimizado, el origen debe eliminar los datos. Para informar al origen de que se ha realizado un movimiento no optimizado:

    -   -   El destino establece el valor de *pdwEffect* recibido a través de su método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) en DROPEFFECT \_ Move. El valor se devolverá al origen mediante [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   El destino también llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos y le pasa un identificador de formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ Move. Esta llamada al método es necesaria porque es posible que algunos destinos de colocación no establezcan correctamente el parámetro *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . El formato de [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) es la forma confiable de indicar que se ha producido un movimiento no optimizado.

5.  El origen inspecciona los dos valores que puede devolver el destino. Si ambos están establecidos en DROPEFFECT \_ Move, se completa el movimiento no optimizado mediante la eliminación de los datos originales. De lo contrario, el destino tenía un movimiento optimizado y se eliminaron los datos originales.

## <a name="handling-delete-on-paste-operations"></a>Control de operaciones de eliminación y pegado

**Escenario:** Uno o varios archivos se cortan de una carpeta en el explorador de Windows y se pegan en una extensión de espacio de nombres. El explorador de Windows deja los archivos resaltados hasta recibir comentarios sobre el resultado de la operación de pegado.

Tradicionalmente, cuando un usuario corta datos, desaparece inmediatamente de la vista. Esto puede no ser eficaz y puede dar lugar a problemas de facilidad de uso si el usuario se preocupa de lo que ha ocurrido en los datos. Un enfoque alternativo es usar una operación de eliminación al pegar.

Con una operación de eliminación en pegado, los datos seleccionados no se quitan de la vista inmediatamente. En su lugar, la aplicación de origen la marca como seleccionada, quizás cambiando la fuente o el color de fondo. Una vez que la aplicación de destino ha pegado los datos, notifica al origen el resultado de la operación. Si el destino realizó un [movimiento optimizado](#handling-optimized-move-operations), el origen puede simplemente actualizar su presentación. Si el destino realizó un movimiento normal, el origen también debe eliminar su copia de los datos. Si se produce un error en la copia, la aplicación de origen restaura los datos seleccionados a su apariencia original.

> [!Note]  
> Normalmente, el shell usa la operación de eliminar al pegar cuando se usa una operación de cortar y pegar para trasladar archivos. Las operaciones de eliminación y pegado con objetos de Shell suelen usar un [movimiento optimizado](#handling-optimized-move-operations) para trasladar los archivos. Para controlar correctamente la transferencia de datos de Shell, la aplicación debe ser capaz de detectar y controlar las operaciones de eliminación en el mismo.

 

El requisito esencial para eliminar al pegar es que el destino debe notificar el resultado de la operación al origen. Sin embargo, las técnicas del portapapeles estándar no se pueden utilizar para implementar la eliminación al pegar porque no proporcionan una manera para que el destino se comunique con el origen. En su lugar, la aplicación de destino usa el método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para notificar el resultado al objeto de datos. A continuación, el objeto de datos puede comunicarse con el origen a través de una interfaz privada.

El procedimiento básico para una operación de eliminación en pegado es el siguiente:

1.  El origen marca la presentación en pantalla de los datos seleccionados.
2.  El origen crea un objeto de datos. Indica una operación de cortar agregando el formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) con un valor de datos de DROPEFFECT \_ Move.
3.  El origen coloca el objeto de datos en el portapapeles mediante [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard).
4.  El destino recupera el objeto de datos del portapapeles mediante [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard).
5.  El destino extrae los datos de [ \_ PREFERREDDROPEFFECT de CFSTR](clipboard.md) . Si se establece en solo DROPEFFECT \_ Move, el destino puede realizar un movimiento optimizado o simplemente copiar los datos.
6.  Si el destino no realiza un movimiento optimizado, llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con el formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ Move.
7.  Una vez completada la función de pegar, el destino llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con el formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) establecido en DROPEFFECT \_ Move.
8.  Cuando se llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con el formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) establecido en DROPEFFECT \_ Move, debe comprobar si también se ha recibido el formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ Move. Si el destino envía ambos formatos, el origen tendrá que eliminar los datos. Si solo se recibe el formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) , el origen puede quitar simplemente los datos de su pantalla. Si se produce un error en la transferencia, el origen actualiza la presentación a su apariencia original.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Transferencia de datos hacia y desde carpetas virtuales

**Escenario:** Un usuario arrastra un objeto o lo coloca en una carpeta virtual.

Las carpetas virtuales contienen objetos que normalmente no forman parte del sistema de archivos. Algunas carpetas virtuales, como la papelera de reciclaje, pueden representar los datos que se almacenan en el disco duro, pero no los objetos normales del sistema de archivos. Algunos pueden representar datos almacenados que se encuentran en un sistema remoto, como un PC de mano o un sitio FTP. Otros, como la carpeta Impresoras, contienen objetos que no representan datos almacenados. Aunque algunas carpetas virtuales forman parte del sistema, los desarrolladores también pueden crear e instalar carpetas virtuales personalizadas mediante la implementación de una extensión de espacio de nombres.

Independientemente del tipo de datos o de su almacenamiento, el shell presenta los objetos de carpeta y archivo contenidos en una carpeta virtual como si fueran archivos y carpetas normales. Es responsabilidad de la carpeta virtual tomar cualquier dato que contenga y presentarlo correctamente en el shell. Este requisito significa que las carpetas virtuales normalmente admiten las transferencias de datos de arrastrar y colocar y del portapapeles.

Por tanto, hay dos grupos de desarrolladores que deben preocuparse de la transferencia de datos a y desde las carpetas virtuales:

-   Desarrolladores cuyas aplicaciones necesitan aceptar datos que se transfieren de una carpeta virtual.
-   Desarrolladores cuyas extensiones de espacio de nombres necesitan admitir correctamente la transferencia de datos.

### <a name="accepting-data-from-a-virtual-folder"></a>Aceptar datos de una carpeta virtual

Las carpetas virtuales pueden representar prácticamente cualquier tipo de datos y pueden almacenar los datos de la forma que elijan. Algunas carpetas virtuales pueden contener archivos y carpetas normales del sistema de archivos. Por ejemplo, otros pueden empaquetar todos sus objetos en un único documento o base de datos.

Cuando se transfiere un objeto de sistema de archivos a una aplicación, el objeto de datos normalmente contiene un formato [CF \_ HDROP](clipboard.md) con la ruta de acceso completa del objeto. La aplicación puede extraer esta cadena y usar las funciones normales del sistema de archivos para abrir el archivo y extraer sus datos. Sin embargo, dado que las carpetas virtuales normalmente no contienen objetos normales del sistema de archivos, normalmente no usan [CF \_ HDROP](clipboard.md).

En lugar de [CF \_ HDROP](clipboard.md), los datos se transfieren normalmente de las carpetas virtuales con los formatos [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md) . El formato [CFSTR \_ FILECONTENTS](clipboard.md) tiene dos ventajas respecto a [CF \_ HDROP](clipboard.md):

-   No se presupone ningún método determinado de almacenamiento de datos.
-   El formato es más flexible. Admite tres mecanismos de transferencia de datos: un objeto de memoria global, una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o una interfaz [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Los objetos de memoria global se suelen usar para transferir datos hacia o desde objetos virtuales porque los datos se deben copiar en la memoria en su totalidad. La transferencia de un puntero de interfaz requiere casi memoria y es mucho más eficaz. Con archivos muy grandes, un puntero de interfaz puede ser el único mecanismo de transferencia de datos práctico. Normalmente, los datos se representan mediante un puntero [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , ya que la interfaz es algo más flexible que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage). El destino extrae el puntero del objeto de datos y usa los métodos de interfaz para extraer los datos.

Para obtener más información sobre cómo administrar los formatos de [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md) , consulte [uso del \_ formato CFSTR FILECONTENTS para extraer datos de un archivo](/windows).

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Transferir datos hacia y desde una extensión de espacio de nombres

Cuando implemente una extensión de espacio de nombres, normalmente querrá admitir funciones de arrastrar y colocar. Siga las recomendaciones para los orígenes y destinos de colocación descritos en [directrices generales](#general-guidelines). En concreto, una extensión de espacio de nombres debe:

-   Ser capaz de administrar los formatos FILECONTENTS de [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [ \_ CFSTR](clipboard.md) . Estos dos formatos se utilizan normalmente para transferir objetos a y desde extensiones de espacio de nombres.
-   Ser capaz de controlar los [movimientos optimizados](#handling-optimized-move-operations). El shell espera que los objetos de Shell se muevan con un movimiento optimizado.
-   Ser capaz de controlar una operación de [eliminación en pegado](#handling-delete-on-paste-operations) . El shell usa la operación de eliminar al pegar cuando los objetos se mueven desde el shell con una operación de cortar y pegar.
-   Ser capaz de controlar la transferencia de datos a través de una interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . La transferencia de datos a o desde una carpeta virtual se controla normalmente transfiriendo uno de estos dos punteros de interfaz, normalmente un puntero **IStream** . A continuación, el destino llama a los métodos de interfaz para extraer los datos:
    -   -   Como origen de colocación, la extensión de espacio de nombres debe extraer los datos del almacenamiento y pasarlos a través de esta interfaz al destino.
        -   Como destino de colocación, una extensión de espacio de nombres debe aceptar datos de un origen a través de esta interfaz y almacenarlos correctamente.

## <a name="dropping-files-on-the-recycle-bin"></a>Quitar archivos de la papelera de reciclaje

**Escenario:** El usuario coloca un archivo en la **papelera de reciclaje**. La extensión de la aplicación o el espacio de nombres elimina el archivo original.

La papelera de reciclaje es una carpeta virtual que se usa como repositorio para los archivos que ya no son necesarios. Siempre que no se haya vaciado la papelera de reciclaje, el usuario puede recuperar el archivo más adelante y devolverlo al sistema de archivos.

En su mayor parte, la transferencia de objetos de Shell a la papelera de reciclaje funciona de forma muy parecida a cualquier otra carpeta. Sin embargo, cuando un usuario coloca un archivo en la **papelera de reciclaje**, el origen debe eliminar el original, incluso aunque los comentarios de la carpeta indiquen una operación de copia. Normalmente, un origen de colocación no tiene forma alguna de saber en qué carpeta se ha quitado su objeto de datos. Sin embargo, para los sistemas Windows 2000 y versiones posteriores, cuando se coloca un objeto de datos en la **papelera de reciclaje**, el shell llamará al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos con un formato [CFSTR \_ TARGETCLSID](clipboard.md) establecido en el identificador de clase (CLSID) de la papelera de reciclaje (CLSID \_ RecycleBin). Para controlar correctamente el caso de la papelera de reciclaje, el objeto de datos debe ser capaz de reconocer este formato y comunicar la información al origen a través de una interfaz privada.

> [!Note]  
> Cuando se llama a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con un formato [CFSTR \_ TARGETCLSID](clipboard.md) establecido en CLSID \_ RecycleBin, el origen de datos debe cerrar todos los identificadores abiertos a los objetos que se van a transferir antes de volver del método. De lo contrario, podría crear infracciones de uso compartido.

 

## <a name="creating-and-importing-scrap-files"></a>Crear e importar archivos de rechazo

**Escenario:** Un usuario arrastra algunos datos desde el archivo de datos de una aplicación OLE y los coloca en el escritorio o en el explorador de Windows.

Windows permite a los usuarios arrastrar un objeto desde el archivo de datos de una aplicación OLE y colocarlo en el escritorio o en una carpeta del sistema de archivos. Esta operación crea un *archivo de recorte*, que contiene los datos o un vínculo a los datos. El nombre de archivo se toma del nombre corto registrado para el CLSID del objeto y los datos [de \_ texto de CF](clipboard.md) . Para que el shell cree un archivo de recorte que contiene datos, la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de la aplicación debe admitir el \_ formato del portapapeles de EMBEDSOURCE de CF. Para crear un archivo que contenga un vínculo, **IDataObject** debe admitir el \_ formato CF LINKSOURCE.

También hay tres características opcionales que una aplicación puede implementar para admitir archivos de recorte:

-   Compatibilidad con acciones de ida y vuelta
-   Formatos de datos almacenados en caché
-   Representación diferida

### <a name="round-trip-support"></a>Compatibilidad con acciones de ida y vuelta

Un *recorrido de ida* y vuelta implica la transferencia de un objeto de datos a otro contenedor y, a continuación, de nuevo al documento original. Por ejemplo, un usuario podría transferir un grupo de celdas de una hoja de cálculo al escritorio, creando un archivo de recorte con los datos. Si el usuario transfiere el recorte a la hoja de cálculo, los datos deben integrarse en el documento tal como estaba antes de la transferencia original.

Cuando el shell crea el archivo de recorte, representa los datos como un objeto de incrustación. Cuando el residuo se transfiere a otro contenedor, se transfiere como un objeto de incrustación, aunque se devuelva al documento original. La aplicación es responsable de determinar el formato de datos contenido en el rechazo y de volver a colocar los datos en su formato nativo, si es necesario.

Para establecer el formato del objeto incrustado, determine su CLSID recuperando el formato CF OBJECTDESCRIPTOR del objeto \_ . Si el CLSID indica un formato de datos que pertenece a la aplicación, debe transferir los datos nativos en lugar de llamar a [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata).

### <a name="cached-data-formats"></a>Formatos de datos almacenados en caché

Cuando el shell crea un archivo de recorte, comprueba el registro para obtener la lista de formatos disponibles. De forma predeterminada, hay dos formatos disponibles: CF \_ EMBEDSOURCE y CF \_ LINKSOURCE. Sin embargo, hay una serie de escenarios en los que es posible que las aplicaciones necesiten tener archivos de recorte en diferentes formatos:

-   Para permitir que los residuos se transfieran a contenedores que no son de OLE, que no admiten formatos de objetos incrustados.
-   Para permitir que los conjuntos de aplicaciones se comuniquen con un formato privado.
-   Para facilitar el control de los recorridos de ida y vuelta.

Las aplicaciones pueden agregar formatos al rechazo mediante su almacenamiento en caché en el registro. Hay dos tipos de formatos almacenados en caché:

-   Formatos de caché de prioridad. En estos formatos, los datos se copian en su totalidad en el rechazo del objeto de datos.
-   Formatos representados por retraso. En estos formatos, el objeto de datos no se copia en el rechazo. En su lugar, la representación se retrasa hasta que un destino solicita los datos. Delay: la representación se describe con más detalle en la sección siguiente.

Para agregar una memoria caché de prioridad o un formato representado por retraso, cree una subclave **dataFormat** en la clave **CLSID** de la aplicación que es el origen de los datos. En esa subclave, cree una subclave **PriorityCacheFormats** o **DelayRenderFormats** . Para cada formato de caché de prioridad o representada por retraso, cree una subclave numerada a partir de cero. Establezca el valor de esta clave en una cadena con el nombre registrado del formato o un \# valor x, donde X representa el número de formato de un formato estándar del portapapeles.

En el ejemplo siguiente se muestran los formatos almacenados en caché para dos aplicaciones. La aplicación MyProg1 tiene el formato de texto enriquecido como formato de caché de prioridad y un formato privado "mi formato" como formato representado por retraso. La aplicación MyProg2 tiene el formato de mapa de bits de CF \_ ( \# 8 ") como formato de caché de prioridad.

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

Se pueden agregar formatos adicionales mediante la creación de subclaves numeradas adicionales.

### <a name="delayed-rendering"></a>Representación diferida

Un formato de representación retrasado permite a una aplicación crear un archivo de recortes pero retrasar el gasto de representar los datos hasta que los solicite un destino. La interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un residuo proporcionará los formatos de representación retrasados al destino junto con los datos nativos y almacenados en caché. Si el destino solicita un formato de representación retrasado, el shell ejecutará la aplicación y proporcionará los datos al destino desde el objeto activo.

> [!Note]  
> Dado que la representación retrasada es algo arriesgada, se debe usar con precaución. No funcionará si el servidor no está disponible o en aplicaciones que no estén habilitadas para OLE.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Arrastrar y colocar objetos de Shell de forma asincrónica

**Escenario:** Un usuario transfiere un gran bloque de datos del origen al destino. Para evitar el bloqueo de ambas aplicaciones durante un período de tiempo considerable, el destino extrae los datos de forma asincrónica.

Normalmente, arrastrar y colocar es una operación sincrónica. En resumen:

1.  El origen de colocación llama a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) y bloquea su subproceso principal hasta que la función devuelve. Bloquear el subproceso principal normalmente bloquea el procesamiento de la interfaz de usuario.
2.  Después de llamar al método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) del destino, el destino extrae los datos del objeto de datos en su subproceso principal. Este procedimiento normalmente bloquea el procesamiento de la interfaz de usuario del destino mientras dure el proceso de extracción.
3.  Una vez extraídos los datos, el destino devuelve la llamada a [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , el sistema devuelve [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)y ambos subprocesos pueden continuar.

En Resumen, la transferencia de datos sincrónicos puede bloquear los subprocesos principales de ambas aplicaciones durante un período de tiempo considerable. En concreto, ambos subprocesos deben esperar mientras el destino extrae los datos. Para pequeñas cantidades de datos, el tiempo necesario para extraer los datos es pequeño y la transferencia de datos sincrónica funciona bastante bien. Sin embargo, la extracción sincrónica de grandes cantidades de datos puede provocar retrasos prolongados e interferir con la interfaz de usuario de destino y origen.

La interfaz [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) es una interfaz opcional que puede ser implementada por un objeto de datos. Proporciona al destino de colocación la capacidad de extraer datos del objeto de datos de forma asincrónica en un subproceso en segundo plano. Una vez que la extracción de datos se entrega al subproceso en segundo plano, los subprocesos principales de ambas aplicaciones pueden continuar.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Usar IASyncOperation/IDataObjectAsyncCapability

> [!Note]  
> La interfaz se llamaba originalmente [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)), pero posteriormente se cambió a [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability). De lo contrario, las dos interfaces son idénticas.

 

El propósito de [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) es permitir que el origen de colocación y el destino de colocación negocien si los datos se pueden extraer de forma asincrónica. En el procedimiento siguiente se describe cómo el origen de colocación utiliza la interfaz:

1.  Cree un objeto de datos que exponga [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability).
2.  Llame a [**SetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) con *FDoOpAsync* establecido en **Variant \_ true** para indicar que se admite una operación asincrónica.
3.  Después de que el método [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) devuelva, llame a [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation):
    -   Si se produce un error en la [**inoperación**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) o devuelve **Variant \_ false**, se realiza una transferencia de datos sincrónica normal y finaliza el proceso de extracción de datos. El origen debe realizar cualquier limpieza necesaria y continuar.
    -   Si [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) devuelve **Variant \_ true**, los datos se extraen de forma asincrónica. Las operaciones de limpieza deben controlarse mediante [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).
4.  Libera el objeto de datos.
5.  Una vez completada la transferencia de datos asincrónica, el objeto de datos notifica normalmente al origen a través de una interfaz privada.

En el procedimiento siguiente se describe cómo el destino de colocación usa la interfaz [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) para extraer datos de forma asincrónica:

1.  Cuando el sistema llama a [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop), llame a [**IDataObject:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y solicite una [](/previous-versions//bb776309(v=vs.85)) / interfaz [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) de IAsyncOperation (IID \_ IAsyncOperation/IID \_ IDataObjectAsyncCapability) del objeto de datos.
2.  Llame a [**GetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode). Si el método devuelve **Variant \_ true**, el objeto de datos admite la extracción de datos asincrónica.
3.  Cree un subproceso independiente para controlar la extracción de datos y llamar a [**StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation).
4.  Devuelva la llamada a [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , como lo haría para una operación de transferencia de datos normal. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) devolverá y desbloqueará el origen de colocación. No llame a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para indicar el resultado de una operación de movimiento o eliminación optimizada. Espere hasta que finalice la operación.
5.  Extraiga los datos en el subproceso en segundo plano. El subproceso principal del destino está desbloqueado y disponible para continuar.
6.  Si la transferencia de datos era una operación de [movimiento optimizado](#handling-optimized-move-operations) o [de eliminación en pegado](#handling-delete-on-paste-operations) , llame a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para indicar el resultado.
7.  Notifique al objeto de datos que la extracción ha finalizado mediante una llamada a [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).

 

 
