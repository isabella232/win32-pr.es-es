---
description: En este documento se presentan escenarios comunes de transferencia de datos de Shell y se describe cómo implementar cada uno de ellos en la aplicación.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Control de escenarios de transferencia de datos de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c834768a22ad48a3cc85ec33e79bb1acafb37f0e52537f4be33daee4337a5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057805"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Control de escenarios de transferencia de datos de shell

En [el documento Objeto de datos](dataobject.md) de Shell se ha analizado el enfoque general que se usa para transferir datos de Shell con arrastrar y colocar o el Portapapeles. Sin embargo, para implementar la transferencia de datos de Shell en la aplicación, también debe comprender cómo aplicar estos principios y técnicas generales a las diversas formas en que se pueden transferir los datos de Shell. En este documento se presentan escenarios comunes de transferencia de datos de Shell y se describe cómo implementar cada uno de ellos en la aplicación.

-   [Instrucciones generales](#general-guidelines)
-   [Copiar nombres de archivo desde el Portapapeles a una aplicación](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Extraer los nombres de archivo del objeto de datos](#extracting-the-file-names-from-the-data-object)
-   [Copiar el contenido de un archivo eliminado en una aplicación](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Usar el formato FILECONTENTS de CFSTR \_ para extraer datos de un archivo](/windows)
-   [Control de operaciones de movimiento optimizadas](#handling-optimized-move-operations)
-   [Control de las operaciones de eliminación y pegado](#handling-delete-on-paste-operations)
-   [Transferencia de datos hacia y desde carpetas virtuales](#transfering-data-to-and-from-virtual-folders)
    -   [Aceptar datos de una carpeta virtual](#accepting-data-from-a-virtual-folder)
    -   [Transferencia de datos hacia y desde una extensión NameSpace](#transferring-data-to-and-from-a-namespace-extension)
-   [Quitar archivos en el papelera de reciclaje](#dropping-files-on-the-recycle-bin)
-   [Crear e importar archivos de chat](#creating-and-importing-scrap-files)
    -   [Soporte técnico de ida y vuelta](#round-trip-support)
    -   [Formatos de datos almacenados en caché](#cached-data-formats)
    -   [Representación retrasada](#delayed-rendering)
-   [Arrastrar y colocar objetos de shell de forma asincrónica](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Uso de IASyncOperation/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Aunque cada uno de estos escenarios describe una operación de transferencia de datos específica, muchos de ellos se aplican a una variedad de escenarios relacionados. Por ejemplo, la diferencia principal entre la mayoría de las transferencias del Portapapeles y las transferencias de arrastrar y colocar es cómo llega el objeto de datos al destino. Una vez que el destino tiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos, los procedimientos para extraer información son en gran medida los mismos para ambos tipos de transferencia de datos. Sin embargo, algunos de los escenarios se limitan a un tipo específico de operación. Consulte el escenario individual para obtener más información.

 

## <a name="general-guidelines"></a>Directrices generales

En cada una de las secciones siguientes se describe un escenario de transferencia de datos único y bastante específico. Sin embargo, las transferencias de datos suelen ser más complejas y pueden implicar aspectos de varios escenarios. Normalmente no sabe, de antemano, qué escenario tendrá que controlar realmente. Estas son algunas directrices generales que debe tener en cuenta.

Para orígenes de datos:

-   Los formatos del Portapapeles del shell, a excepción [de CF \_ HDROP,](clipboard.md)no están predefinidos. Cada formato que quiera usar debe registrarse mediante una llamada [a RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Los formatos de los objetos de datos se proporcionan en el orden de preferencia del origen. Enumere el objeto de datos y elija el primero que pueda consumir.
-   Incluya tantos formatos como pueda admitir. Por lo general, no sabe dónde se va a descartar el objeto de datos. Esta práctica mejora las probabilidades de que el objeto de datos contenga un formato que el destino de colocación pueda aceptar.
-   Los archivos existentes se deben ofrecer con el [ \_ formato CF HDROP.](clipboard.md)
-   Ofrezca datos de tipo archivo con [formatos CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR.](clipboard.md) Este enfoque permite al destino crear un archivo a partir de un objeto de datos sin necesidad de saber nada sobre el almacenamiento de datos subyacente. Normalmente, debe presentar los datos como una [**interfaz IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Este mecanismo de transferencia de datos es más flexible que un objeto de memoria global y usa mucha menos memoria.
-   Los orígenes de arrastre deben ofrecer el formato [ \_ SHELLIDLIST de CFSTR](clipboard.md) al arrastrar elementos de Shell. Los objetos de datos de los elementos se pueden adquirir mediante los métodos [**IShellFolder::GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) o [**IShellItem::BindToHandler.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) Los orígenes de datos pueden crear una implementación de objeto de datos estándar que admita el formato [ \_ SHELLIDLIST](clipboard.md) de CFSTR mediante [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject).
-   Los destinos de colocación que quieran razonar sobre los elementos que se arrastran mediante el modelo de programación de elementos de shell pueden convertir un objeto IDataObject en [**un objeto IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) mediante [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).
-   Use cursores de comentarios estándar.
-   Admite arrastrar a la izquierda y a la derecha.
-   Use el propio objeto de datos de un objeto incrustado. Este enfoque permite a la aplicación recuperar los formatos adicionales que ofrece el objeto de datos y evita crear una capa adicional de contención. Por ejemplo, un objeto incrustado del servidor A se arrastra desde el servidor o contenedor B y se descarta en el contenedor C. C debe crear un objeto incrustado del servidor A, no un objeto incrustado del servidor B que contenga un objeto incrustado del servidor A.
-   Recuerde que el Shell puede usar [movimientos optimizados](#handling-optimized-move-operations) o [operaciones de eliminación y](#handling-delete-on-paste-operations) pegado al mover archivos. La aplicación debe ser capaz de reconocer estas operaciones y responder adecuadamente.

Para destinos de datos:

-   Los formatos del Portapapeles del shell, a excepción [de CF \_ HDROP,](clipboard.md)no están predefinidos. Cada formato que quiera usar debe registrarse mediante una llamada [a RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Implemente y registre un destino de colocación OLE. Evite usar Windows destinos 3.1 o el [**mensaje \_ DROPFILES**](wm-dropfiles.md) de WM, si es posible.
-   Los formatos contenidos en un objeto de datos varían, dependiendo de dónde procede el objeto. Puesto que generalmente no sabe de antemano de dónde procede un objeto de datos, no suponga que un formato determinado estará presente. El objeto de datos debe enumerar los formatos en orden de calidad, empezando por el mejor. Por lo tanto, para obtener el mejor formato disponible, las aplicaciones normalmente enumeran los formatos disponibles y usan el primer formato de la enumeración que pueden admitir.
-   Admite el arrastre a la derecha. Puede personalizar el menú contextual de arrastre mediante la creación de un controlador [de arrastrar y colocar](context-menu-handlers.md).
-   Si la aplicación acepta archivos existentes, debe ser capaz de controlar el [formato CF \_ HDROP.](clipboard.md)
-   En general, las aplicaciones que aceptan archivos también deben controlar los [ \_ formatos CFSTR FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR.](clipboard.md) Aunque los archivos del sistema de archivos tienen el formato [ \_ CF HDROP,](clipboard.md) los archivos de proveedores como las extensiones de espacio de nombres suelen usar [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md). Algunos ejemplos son Windows CE carpetas, protocolo de transferencia de archivos (FTP), carpetas web y carpetas CAB. Normalmente, el origen implementa una [**interfaz IStream**](/windows/win32/api/objidl/nn-objidl-istream) para presentar los datos de su almacenamiento como un archivo.
-   Recuerde que el Shell puede usar [movimientos optimizados](#handling-optimized-move-operations) o [operaciones de eliminación y](#handling-delete-on-paste-operations) pegado al mover archivos. La aplicación debe ser capaz de reconocer estas operaciones y responder adecuadamente.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Copiar nombres de archivo desde el Portapapeles a una aplicación

**Escenario:** Un usuario selecciona uno o varios archivos en Windows Explorer y los copia en el Portapapeles. La aplicación extrae los nombres de archivo y los pega en el documento.

Este escenario se podría usar, por ejemplo, para permitir que un usuario cree un vínculo HTML cortando y pegando el archivo en la aplicación. A continuación, la aplicación puede extraer el nombre de archivo del objeto de datos y procesarlo para crear una etiqueta delimitadora.

Cuando un usuario selecciona un archivo en Windows Explorer y lo copia en el Portapapeles, el Shell crea un objeto de datos. A continuación, llama a [**OleSetClipboard para**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) colocar un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el Portapapeles.

Cuando el usuario selecciona el comando **Pegar en** el menú o la barra de herramientas de la aplicación:

1.  Llame [**a OleGetClipboard para**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) recuperar la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
2.  Llame [**a IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) para solicitar un objeto enumerador.
3.  Use la interfaz [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) del objeto enumerador para enumerar los formatos contenidos en el objeto de datos.

> [!Note]  
> Los dos últimos pasos de este procedimiento se incluyen por integridad. Normalmente no son necesarias para transferencias de archivos simples. Todos los objetos de datos utilizados para este tipo de transferencia de datos deben contener el formato [ \_ CF HDROP,](clipboard.md) que se puede usar para determinar los nombres de los archivos contenidos en el objeto. Sin embargo, para transferencias de datos más generales, debe enumerar los formatos y seleccionar el mejor que la aplicación puede controlar.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Extraer los nombres de archivo del objeto de datos

El siguiente paso consiste en extraer uno o varios nombres de archivo del objeto de datos y pegarlos en la aplicación. Tenga en cuenta que el procedimiento descrito en esta sección para extraer un nombre de archivo de un objeto de datos se aplica igualmente bien a las transferencias de arrastrar y colocar.

La manera más sencilla de recuperar nombres de archivo de un objeto de datos es el [formato \_ CF HDROP:](clipboard.md)

1.  Llame [**a IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Establezca el **miembro cfFormat** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en [CF \_ HDROP](clipboard.md) y el miembro **tymed** en [TYMED \_ HGLOBAL](dataobject.md). El **miembro dwAspect** normalmente se establece en DVASPECT \_ CONTENT. Sin embargo, si necesita tener la ruta de acceso del archivo en formato corto (8.3), establezca **dwAspect** en DVASPECT \_ SHORT.

    Cuando [**se devuelve IDataObject::GetData,**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) el **miembro hGlobal** de la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) apunta a un objeto de memoria global que contiene los datos.

2.  Cree una variable HDROP y esta establezca en el **miembro hGlobal** de la [**estructura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) La variable HDROP es ahora un identificador de una estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) seguida de una cadena terminada en null doble que contiene las rutas de acceso de archivo completas de los archivos copiados.
3.  Para determinar cuántas rutas de acceso de archivo hay en la lista, llame a [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) con el parámetro *iFile* establecido en 0xFFFFFFFF. La función devuelve el número de rutas de acceso de archivo de la lista. El índice de base cero de la ruta de acceso de archivo de esta lista se usa en el paso siguiente para identificar una ruta de acceso determinada.
4.  Extraiga las rutas de acceso de archivo del objeto de memoria global llamando a [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) una vez para cada archivo, con *iFile* establecido en el índice del archivo.
5.  Procese las rutas de acceso de archivo según sea necesario y péguelas en la aplicación.
6.  Llame [**a ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) y pase el puntero a la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que pasó a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) en el paso 1. Una vez que haya liberado la estructura, el valor HDROP que creó en el paso 2 ya no es válido y no debe usarse.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Copiar el contenido de un archivo eliminado en una aplicación

**Escenario:** Un usuario arrastra uno o varios archivos desde Windows Explorer y los coloca en la ventana de la aplicación. La aplicación extrae el contenido de los archivos y lo pega en la aplicación.

En este escenario se usa la función de arrastrar y colocar para transferir los archivos desde Windows Explorer a la aplicación. Antes de la operación, la aplicación debe:

1.  Llame [a RegisterClipboardFormat para](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) registrar los formatos necesarios del Portapapeles de Shell.
2.  Llame [**a RegisterDragDrop para**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) registrar una ventana de destino y la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la aplicación.

Después de que el usuario inicie la operación, seleccione uno o varios archivos y empiece a arrastrarlos:

1.  Windows El Explorador crea un objeto de datos y carga los formatos admitidos en él.
2.  Windows El explorador llama [**a DoDragDrop para**](/windows/win32/api/ole2/nf-ole2-dodragdrop) iniciar el bucle de arrastre.
3.  Cuando la imagen de arrastre llega a la ventana de destino, el sistema le notifica mediante una llamada a [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Para determinar qué contiene el objeto de datos, llame al método [**IDataObject::EnumFormatEtc del**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) objeto de datos. Use el objeto enumerador devuelto por el método para enumerar los formatos contenidos en el objeto de datos. Si la aplicación no quiere aceptar ninguno de estos formatos, devuelva DROPEFFECT \_ NONE. Para este escenario, la aplicación debe omitir los objetos de datos que no contengan formatos usados para transferir archivos, como [CF \_ HDROP.](clipboard.md)
5.  Cuando el usuario quita los datos, el sistema llama a [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).
6.  Use la [**interfaz IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extraer el contenido de los archivos.

Hay varias maneras diferentes de extraer el contenido de un objeto Shell de un objeto de datos. En general, use el orden siguiente:

-   Si el archivo contiene un formato [CF \_ TEXT,](clipboard.md) los datos son texto ANSI. Puede usar el formato CF TEXT para extraer los datos, en \_ lugar de abrir el propio archivo.
-   Si el archivo contiene un objeto OLE vinculado o incrustado, el objeto de datos contiene un formato CF \_ EMBEDDEDOBJECT. Use técnicas OLE estándar para extraer los datos. [Los archivos de](#creating-and-importing-scrap-files) desechado siempre contienen un \_ formato CF EMBEDDEDOBJECT.
-   Si el objeto Shell es del sistema de archivos, el objeto de datos contiene un formato [ \_ CF HDROP](clipboard.md) con los nombres de los archivos. Extraiga el nombre de archivo [de CF \_ HDROP](clipboard.md) y llame a [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) para crear un nuevo objeto vinculado o incrustado. Para obtener una explicación sobre cómo recuperar un nombre de archivo de un formato [ \_ CF HDROP,](clipboard.md) vea Copiar nombres de archivo desde el Portapapeles a [una aplicación](#copying-file-names-from-the-clipboard-to-an-application).
-   Si el objeto de datos contiene un formato [ \_ FILEDESCRIPTOR de CFSTR,](clipboard.md) puede extraer el contenido de un archivo del formato [CFSTR \_ FILECONTENTS del](clipboard.md) archivo. Para obtener una explicación de este procedimiento, vea Usar el formato [ \_ FILECONTENTS de CFSTR para extraer datos de un archivo](/windows).
-   Antes de shell versión [4.71,](versions.md)una aplicación indicaba que estaba transfiriendo un tipo de archivo de acceso directo estableciendo **FD \_ LINKUI** en el miembro **dwFlags** de la [**estructura FILEDESCRIPTOR.**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) Para versiones posteriores del shell, la manera preferida de indicar que se transfieren los accesos directos es usar el formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ LINK. Este enfoque es mucho más eficaz que extraer la **estructura FILEDESCRIPTOR** solo para comprobar una marca.

Si el proceso de extracción de datos será largo, puede que desee realizar la operación de forma asincrónica en un subproceso en segundo plano. El subproceso principal puede continuar sin retrasos innecesarios. Para obtener una explicación sobre cómo controlar la extracción asincrónica de datos, vea Arrastrar y quitar objetos [de shell de forma asincrónica.](#dragging-and-dropping-shell-objects-asynchronously)

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Usar el formato FILECONTENTS de CFSTR \_ para extraer datos de un archivo

El [formato \_ FILECONTENTS](clipboard.md) de CFSTR proporciona una manera muy flexible y eficaz de transferir el contenido de un archivo. Ni siquiera es necesario que los datos se almacenen como un solo archivo. Todo lo que se necesita para este formato es que el objeto de datos presente los datos en el destino como si fuera un archivo. Por ejemplo, los datos reales pueden ser una sección de un documento de texto o un bloque de datos extraídos de una base de datos. El destino puede tratar los datos como un archivo y no necesita saber nada sobre el mecanismo de almacenamiento subyacente.

Las extensiones de espacio de nombres suelen [usar CFSTR \_ FILECONTENTS](clipboard.md) para transferir datos, ya que este formato no supone ningún mecanismo de almacenamiento determinado. Una extensión de espacio de nombres puede usar cualquier mecanismo de almacenamiento que sea conveniente y usar este formato para presentar sus objetos a las aplicaciones como si fueran archivos.

El mecanismo de transferencia de datos [para CFSTR \_ FILECONTENTS](clipboard.md) suele [ser TYMED \_ ISTREAM.](dataobject.md) La transferencia de un puntero de interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) requiere mucha menos memoria que cargar los datos en un objeto de memoria global, e **IStream** es una manera más sencilla de representar los datos que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Un [formato \_ FILECONTENTS](clipboard.md) de CFSTR siempre va acompañado de un formato [ \_ FILEDESCRIPTOR de CFSTR.](clipboard.md) Primero debe examinar el contenido de este formato. Si se transfiere más de un archivo, el objeto de datos realmente contendrá varios [ \_ formatos DE ARCHIVO CFSTRCONTENTS,](clipboard.md) uno para cada archivo. El formato [ \_ FILEDESCRIPTOR](clipboard.md) de CFSTR contiene el nombre y los atributos de cada archivo y proporciona un valor de índice para cada archivo necesario para extraer el formato [CFSTR \_ FILECONTENTS](clipboard.md) de un archivo determinado.

Para extraer un [formato \_ FILECONTENTS de CFSTR:](clipboard.md)

1.  Extraiga el [formato \_ FILEDESCRIPTOR de CFSTR](clipboard.md) como un [valor de TYMED \_ HGLOBAL.](dataobject.md)
2.  El **miembro hGlobal** de la estructura [**STGMEDIUM devuelta**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) apunta a un objeto de memoria global. Bloquee ese objeto pasando el **valor hGlobal** a [**GlobalLock.**](/windows/win32/api/winbase/nf-winbase-globallock)
3.  Convierte el puntero devuelto por [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) en un [**puntero FILEGROUPDESCRIPTOR.**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) Apuntará a una **estructura FILEGROUPDESCRIPTOR** seguida de una o varias [**estructuras FILEDESCRIPTOR.**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) Cada **estructura FILEDESCRIPTOR** contiene una descripción de un archivo contenido en uno de los formatos [DE \_ ARCHIVOCONTENTS de CFSTR que](clipboard.md) lo acompañan.
4.  Examine las [**estructuras FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para determinar cuál corresponde al archivo que desea extraer. El índice de base cero de esa **estructura FILEDESCRIPTOR** se usa para identificar el formato [CFSTR \_ FILECONTENTS del](clipboard.md) archivo. Dado que el tamaño de un bloque de memoria global no es preciso en bytes, use los miembros **nFileSizeLow** y **nFileSizeHigh** de la estructura para determinar cuántos bytes representan el archivo en el objeto de memoria global.
5.  Llame [**a IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con el miembro **cfFormat** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) establecido en el valor [ \_ FILECONTENTS](clipboard.md) de CFSTR y el miembro **lIndex** establecido en el índice que determinó en el paso anterior. El **miembro tymed** normalmente se establece en [TYMED \_ HGLOBAL](dataobject.md) \| TYMED \_ ISTREAM \| TYMED \_ ISTORAGE. A continuación, el objeto de datos puede elegir su mecanismo de transferencia de datos preferido.
6.  La [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que [**devuelve IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) contendrá un puntero a los datos del archivo. Examine el **miembro tymed** de la estructura para determinar el mecanismo de transferencia de datos.
7.  Si **tymed** está establecido en [TYMED \_ ISTREAM](dataobject.md) o TYMED \_ ISTORAGE, use la interfaz para extraer los datos. Si **tymed** se establece en TYMED \_ HGLOBAL, los datos se incluyen en un objeto de memoria global. Para obtener una explicación sobre cómo extraer datos de un objeto de memoria global, vea la sección Extracción de un objeto de memoria *global de* un objeto de datos del objeto de datos [de shell](dataobject.md).
8.  Llame [**a GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) para desbloquear el objeto de memoria global que bloqueó en el paso 2.

## <a name="handling-optimized-move-operations"></a>Control de operaciones de movimiento optimizadas

**Escenario:** Un archivo se mueve del sistema de archivos a una extensión de espacio de nombres mediante un movimiento optimizado.

En una operación de movimiento convencional, el destino realiza una copia de los datos y el origen elimina el original. Este procedimiento puede ser ineficaz porque requiere dos copias de los datos. Con objetos grandes como bases de datos, es posible que una operación de movimiento convencional ni siquiera sea práctica.

Con un movimiento optimizado, el destino usa su comprensión de cómo se almacenan los datos para controlar toda la operación de movimiento. Nunca hay una segunda copia de los datos y no es necesario que el origen elimine los datos originales. Los datos de shell son adecuados para los movimientos optimizados porque el destino puede controlar toda la operación mediante shell API. Un ejemplo típico es mover archivos. Una vez que el destino tiene la ruta de acceso de un archivo que se va a mover, puede usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para moverlo. No es necesario que el origen elimine el archivo original.

> [!Note]  
> El shell normalmente usa un movimiento optimizado para mover archivos. Para controlar correctamente la transferencia de datos de Shell, la aplicación debe ser capaz de detectar y controlar un movimiento optimizado.

 

Los movimientos optimizados se controlan de la siguiente manera:

1.  El origen llama [**a DoDragDrop con**](/windows/win32/api/ole2/nf-ole2-dodragdrop) el *parámetro dwEffect* establecido en DROPEFFECT MOVE para indicar que se pueden mover los objetos \_ de origen.
2.  El destino recibe el valor DROPEFFECT MOVE a través de uno de sus \_ [**métodos IDropTarget,**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) lo que indica que se permite un movimiento.
3.  El destino copia el objeto (movimiento no optimizado) o lo mueve (movimiento optimizado).
4.  A continuación, el destino indica al origen si necesita eliminar los datos originales.

    Un movimiento optimizado es la operación predeterminada, con los datos eliminados por el destino. Para informar al origen de que se realizó un movimiento optimizado:

    -   -   El destino establece el *valor pdwEffect* que recibió a través de su método [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) en un valor distinto de DROPEFFECT \_ MOVE. Normalmente se establece en DROPEFFECT \_ NONE o DROPEFFECT \_ COPY. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)devolverá el valor al origen.
        -   El destino también llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos y le pasa un identificador de formato [ \_ CFSTR PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ NONE. Esta llamada al método es necesaria porque algunos destinos de colocación podrían no establecer correctamente el *parámetro pdwEffect* [**de DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop) El [formato CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) es la manera confiable de indicar que se ha realizado un movimiento optimizado.

    Si el destino ha hecho un movimiento sin optimizar, el origen debe eliminar los datos. Para informar al origen de que se ha realizado un movimiento sin optimizar:

    -   -   El destino establece el *valor pdwEffect* que recibió a través de su [**método IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) en DROPEFFECT \_ MOVE. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)devolverá el valor al origen.
        -   El destino también llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos y le pasa un identificador de formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ MOVE. Esta llamada al método es necesaria porque algunos destinos de colocación podrían no establecer correctamente el *parámetro pdwEffect* [**de DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop) El [formato CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) es la manera confiable de indicar que se ha realizado un movimiento sin optimizar.

5.  El origen inspecciona los dos valores que puede devolver el destino. Si ambos se establecen en DROPEFFECT MOVE, completa el movimiento sin optimizar mediante \_ la eliminación de los datos originales. De lo contrario, el destino ha realizado un movimiento optimizado y se han eliminado los datos originales.

## <a name="handling-delete-on-paste-operations"></a>Control de las operaciones de eliminación y pegado

**Escenario:** Uno o varios archivos se cortan de una carpeta en Windows Explorer y se pegan en una extensión de espacio de nombres. Windows El Explorador deja los archivos resaltados hasta que recibe comentarios sobre el resultado de la operación de pegado.

Tradicionalmente, cuando un usuario corta datos, desaparece inmediatamente de la vista. Esto podría no ser eficaz y puede provocar problemas de facilidad de uso si el usuario se preocupa por lo que ha ocurrido con los datos. Un enfoque alternativo es usar una operación de eliminación y pegado.

Con una operación de eliminación y pegado, los datos seleccionados no se quitan inmediatamente de la vista. En su lugar, la aplicación de origen lo marca como seleccionado, quizás cambiando la fuente o el color de fondo. Una vez que la aplicación de destino ha pegar los datos, notifica al origen el resultado de la operación. Si el destino realizó un [movimiento optimizado,](#handling-optimized-move-operations)el origen puede simplemente actualizar su presentación. Si el destino realizó un movimiento normal, el origen también debe eliminar su copia de los datos. Si se produce un error en el pegado, la aplicación de origen restaura los datos seleccionados a su apariencia original.

> [!Note]  
> Normalmente, el Shell usa eliminar y pegar cuando se usa una operación de cortar y pegar para mover archivos. Las operaciones de eliminación y pegado con objetos de Shell normalmente usan un [movimiento optimizado](#handling-optimized-move-operations) para mover los archivos. Para controlar correctamente la transferencia de datos de Shell, la aplicación debe ser capaz de detectar y controlar las operaciones de eliminación y pegado.

 

El requisito esencial para eliminar y pegar es que el destino debe notificar el resultado de la operación al origen. Sin embargo, las técnicas estándar del Portapapeles no se pueden usar para implementar delete-on-paste porque no proporcionan una manera de que el destino se comunique con el origen. En su lugar, la aplicación de destino usa el método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para notificar el resultado al objeto de datos. A continuación, el objeto de datos puede comunicarse con el origen a través de una interfaz privada.

El procedimiento básico para una operación de eliminación y pegado es el siguiente:

1.  El origen marca la pantalla de los datos seleccionados.
2.  El origen crea un objeto de datos. Indica una operación de corte agregando el formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) con un valor de datos DROPEFFECT \_ MOVE.
3.  El origen coloca el objeto de datos en el Portapapeles mediante [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard).
4.  El destino recupera el objeto de datos del Portapapeles mediante [**OleGetClipboard.**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)
5.  El destino extrae los datos [DE CFSTR \_ PREFERREDDROPEFFECT.](clipboard.md) Si se establece en solo DROPEFFECT MOVE, el destino puede realizar un movimiento \_ optimizado o simplemente copiar los datos.
6.  Si el destino no realiza un movimiento optimizado, llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con el formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ MOVE.
7.  Una vez completado el pegado, el destino llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con el formato [ \_ CFSTR PASTESUCCEEDED](clipboard.md) establecido en DROPEFFECT \_ MOVE.
8.  Cuando se llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con el formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) establecido en DROPEFFECT MOVE, debe comprobar si también recibió el formato \_ [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) establecido en DROPEFFECT \_ MOVE. Si el destino envía ambos formatos, el origen tendrá que eliminar los datos. Si solo se [recibe el \_ formato CFSTR PASTESUCCEEDED,](clipboard.md) el origen puede simplemente quitar los datos de su pantalla. Si se produce un error en la transferencia, el origen actualiza la pantalla a su apariencia original.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Transferencia de datos hacia y desde carpetas virtuales

**Escenario:** Un usuario arrastra un objeto o lo coloca en una carpeta virtual.

Las carpetas virtuales contienen objetos que generalmente no forman parte del sistema de archivos. Algunas carpetas virtuales, como papelera de reciclaje, pueden representar datos almacenados en el disco duro, pero no como objetos normales del sistema de archivos. Algunos pueden representar datos almacenados que se encuentra en un sistema remoto, como un equipo portátil o un sitio FTP. Otros, como la carpeta Impresoras, contienen objetos que no representan datos almacenados en absoluto. Aunque algunas carpetas virtuales forman parte del sistema, los desarrolladores también pueden crear e instalar carpetas virtuales personalizadas mediante la implementación de una extensión de espacio de nombres.

Independientemente del tipo de datos o de cómo se almacenan, el Shell presenta los objetos de carpeta y archivo que contiene una carpeta virtual como si fueran archivos y carpetas normales. Es responsabilidad de la carpeta virtual tomar los datos que contiene y presentarlo al Shell de forma adecuada. Este requisito significa que las carpetas virtuales normalmente admiten las transferencias de datos de arrastrar y colocar y del Portapapeles.

Por lo tanto, hay dos grupos de desarrolladores que deben preocuparse por la transferencia de datos hacia y desde carpetas virtuales:

-   Desarrolladores cuyas aplicaciones necesitan aceptar datos transferidos desde una carpeta virtual.
-   Desarrolladores cuyas extensiones de espacio de nombres deben admitir correctamente la transferencia de datos.

### <a name="accepting-data-from-a-virtual-folder"></a>Aceptar datos de una carpeta virtual

Las carpetas virtuales pueden representar prácticamente cualquier tipo de datos y almacenar los datos de la manera que elijan. Algunas carpetas virtuales pueden contener archivos y carpetas normales del sistema de archivos. Otros pueden, por ejemplo, empaquetar todos sus objetos en un único documento o base de datos.

Cuando un objeto del sistema de archivos se transfiere a una aplicación, el objeto de datos normalmente contiene un formato [ \_ CF HDROP](clipboard.md) con la ruta de acceso completa del objeto. La aplicación puede extraer esta cadena y usar las funciones normales del sistema de archivos para abrir el archivo y extraer sus datos. Sin embargo, dado que las carpetas virtuales normalmente no contienen objetos normales del sistema de archivos, por lo general no usan [CF \_ HDROP](clipboard.md).

En lugar [de CF \_ HDROP,](clipboard.md)los datos se transfieren normalmente desde carpetas virtuales con los formatos [ \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS de](clipboard.md) CFSTR. El [formato \_ FILECONTENTS de CFSTR](clipboard.md) tiene dos ventajas con respecto a CF [ \_ HDROP:](clipboard.md)

-   No se supone ningún método concreto de almacenamiento de datos.
-   El formato es más flexible. Admite tres mecanismos de transferencia de datos: un objeto de memoria global, una [**interfaz IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**una interfaz IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage)

Los objetos de memoria global rara vez se usan para transferir datos hacia o desde objetos virtuales, ya que los datos se deben copiar en la memoria en su totalidad. La transferencia de un puntero de interfaz no requiere casi memoria y es mucho más eficaz. Con archivos muy grandes, un puntero de interfaz podría ser el único mecanismo práctico de transferencia de datos. Normalmente, los datos se representan mediante un [**puntero IStream,**](/windows/win32/api/objidl/nn-objidl-istream) porque esa interfaz es algo más flexible que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage). El destino extrae el puntero del objeto de datos y usa los métodos de interfaz para extraer los datos.

Para obtener más información sobre cómo controlar los formatos [ \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS de CFSTR,](clipboard.md) vea [Using the CFSTR \_ FILECONTENTS Format to Extract Data from a File](/windows).

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Transferencia de datos hacia y desde una extensión NameSpace

Al implementar una extensión de espacio de nombres, normalmente querrá admitir funcionalidades de arrastrar y colocar. Siga las recomendaciones para quitar orígenes y destinos que se deban a las [directrices generales.](#general-guidelines) En concreto, una extensión de espacio de nombres debe:

-   Puede controlar los formatos [ \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS de CFSTR.](clipboard.md) Estos dos formatos se usan normalmente para transferir objetos hacia y desde extensiones de espacio de nombres.
-   Ser capaz de controlar los [movimientos optimizados.](#handling-optimized-move-operations) Shell espera que los objetos de Shell se muevan con un movimiento optimizado.
-   Ser capaz de controlar una [operación de eliminación y](#handling-delete-on-paste-operations) pegado. El Shell usa eliminar y pegar cuando los objetos se mueven desde el shell con una operación de cortar y pegar.
-   Ser capaz de controlar la transferencia de datos a través de [**una interfaz IStream**](/windows/win32/api/objidl/nn-objidl-istream) [**o IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) Normalmente, la transferencia de datos hacia o desde una carpeta virtual se controla mediante la transferencia de uno de estos dos punteros de interfaz, normalmente un **puntero IStream.** A continuación, el destino llama a los métodos de interfaz para extraer los datos:
    -   -   Como origen de colocación, la extensión de espacio de nombres debe extraer los datos del almacenamiento y pasarlo a través de esta interfaz al destino.
        -   Como destino de colocación, una extensión de espacio de nombres debe aceptar datos de un origen a través de esta interfaz y almacenarlo correctamente.

## <a name="dropping-files-on-the-recycle-bin"></a>Quitar archivos en el papelera de reciclaje

**Escenario:** El usuario quita un archivo en el **papelera de reciclaje**. La extensión de la aplicación o del espacio de nombres elimina el archivo original.

El papelera de reciclaje es una carpeta virtual que se usa como repositorio para los archivos que ya no son necesarios. Siempre que el papelera de reciclaje se haya vaciado, el usuario puede recuperar más adelante el archivo y devolverlo al sistema de archivos.

En su mayor parte, la transferencia de objetos de Shell al papelera de reciclaje funciona de forma muy parecido a cualquier otra carpeta. Sin embargo, cuando un usuario quita un archivo en el papelera de reciclaje **,** el origen debe eliminar el original, incluso si los comentarios de la carpeta indican una operación de copia. Normalmente, un origen de colocación no tiene forma de saber en qué carpeta se ha eliminado su objeto de datos. Sin embargo, para Windows 2000 y sistemas posteriores, cuando se coloca un objeto de datos en **el papelera de reciclaje**, el shell llamará al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos con un formato [ \_ TARGETCLSID](clipboard.md) de CFSTR establecido en el identificador de clase (CLSID) del papelera de reciclaje (CLSID \_ RecycleBin). Para controlar el papelera de reciclaje caso correctamente, el objeto de datos debe ser capaz de reconocer este formato y comunicar la información al origen a través de una interfaz privada.

> [!Note]  
> Cuando se llama a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con un formato [ \_ TARGETCLSID](clipboard.md) de CFSTR establecido en CLSID RecycleBin, el origen de datos debe cerrar los identificadores abiertos a los objetos que se transfieren antes de volver del \_ método . De lo contrario, podría crear infracciones de uso compartido.

 

## <a name="creating-and-importing-scrap-files"></a>Creación e importación de archivos de chatarra

**Escenario:** Un usuario arrastra algunos datos del archivo de datos de una aplicación OLE y los coloca en el escritorio o Windows Explorer.

Windows permite a los usuarios arrastrar un objeto desde el archivo de datos de una aplicación OLE y colocarlo en el escritorio o en una carpeta del sistema de archivos. Esta operación crea un *archivo de desechado*, que contiene los datos o un vínculo a los datos. El nombre de archivo se toma del nombre corto registrado para el CLSID del objeto y los datos [de CF \_ TEXT.](clipboard.md) Para que el Shell cree un archivo desechado que contenga datos, la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de la aplicación debe admitir el formato del Portapapeles \_ CF EMBEDSOURCE. Para crear un archivo que contenga un vínculo, **IDataObject** debe admitir el formato CF \_ LINKSOURCE.

También hay tres características opcionales que una aplicación puede implementar para admitir archivos de desechado:

-   Soporte técnico de ida y vuelta
-   Formatos de datos almacenados en caché
-   Representación retrasada

### <a name="round-trip-support"></a>Soporte técnico de ida y vuelta

Un *recorrido de ida y* vuelta implica transferir un objeto de datos a otro contenedor y, a continuación, volver al documento original. Por ejemplo, un usuario podría transferir un grupo de celdas de una hoja de cálculo al escritorio, creando un archivo de chat con los datos. Si el usuario transfiere la chatarra de vuelta a la hoja de cálculo, los datos deben integrarse en el documento tal como estaba antes de la transferencia original.

Cuando el Shell crea el archivo de desechado, representa los datos como un objeto de inserción. Cuando la chatarra se transfiere a otro contenedor, se transfiere como un objeto de inserción, incluso si se devuelve al documento original. La aplicación es responsable de determinar el formato de datos contenido en la recopilación y de devolver los datos a su formato nativo si es necesario.

Para establecer el formato del objeto incrustado, determine su CLSID recuperando el formato \_ CF OBJECTDESCRIPTOR del objeto. Si el CLSID indica un formato de datos que pertenece a la aplicación, debe transferir los datos nativos en lugar de llamar a [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata).

### <a name="cached-data-formats"></a>Formatos de datos almacenados en caché

Cuando el Shell crea un archivo de desechado, comprueba en el Registro la lista de formatos disponibles. De forma predeterminada, hay dos formatos disponibles: CF \_ EMBEDSOURCE y CF \_ LINKSOURCE. Sin embargo, hay una serie de escenarios en los que es posible que las aplicaciones necesiten tener archivos de chat en formatos diferentes:

-   Para permitir que los rechazos se transfieran a contenedores que no son OLE, que no pueden aceptar formatos de objeto incrustados.
-   Para permitir que los conjuntos de aplicaciones se comuniquen con un formato privado.
-   Para facilitar el control de los recorridos de ida y vuelta.

Las aplicaciones pueden agregar formatos a la chatarra almacenando en caché en el Registro. Hay dos tipos de formatos almacenados en caché:

-   Formatos de caché de prioridad. Para estos formatos, los datos se copian en su totalidad en la chata del objeto de datos.
-   Formatos con representación retrasada. Para estos formatos, el objeto de datos no se copia en la chatarra. En su lugar, la representación se retrasa hasta que un destino solicita los datos. La representación retrasada se describe con más detalle en la sección siguiente.

Para agregar una caché de prioridad o un formato con representación retrasada, cree una subclave **DataFormat** bajo la clave **CLSID** de la aplicación que es el origen de los datos. En esa subclave, cree una subclave **PriorityCacheFormats** **o DelayRenderFormats.** Para cada caché de prioridad o formato con representación retrasada, cree una subclave numerada a partir de cero. Establezca el valor de esta clave en una cadena con el nombre registrado del formato o en un valor X, donde X representa el número de formato de un formato estándar \# del Portapapeles.

En el ejemplo siguiente se muestran los formatos almacenados en caché para dos aplicaciones. La aplicación MyProg1 tiene el formato de texto enriquecido como formato de caché de prioridad y un formato privado "My Format" como formato de representación retrasada. La aplicación MyProg2 tiene el formato \_ CF BITMAP ( \# 8") como formato de caché de prioridad.

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

### <a name="delayed-rendering"></a>Representación retrasada

Un formato de representación retrasada permite a una aplicación crear un archivo de chat pero retrasar los gastos de representación de los datos hasta que un destino lo solicite. La [**interfaz IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un elemento scrap ofrecerá los formatos de representación retrasados al destino junto con datos nativos y almacenados en caché. Si el destino solicita un formato de representación retrasada, el Shell ejecutará la aplicación y proporcionará los datos al destino desde el objeto activo.

> [!Note]  
> Dado que la representación retrasada es un poco arriesgada, se debe usar con precaución. No funcionará si el servidor no está disponible o en aplicaciones que no están habilitadas para OLE.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Arrastrar y quitar objetos de shell de forma asincrónica

**Escenario:** Un usuario transfiere un gran bloque de datos del origen al destino. Para evitar el bloqueo de ambas aplicaciones durante una cantidad significativa de tiempo, el destino extrae los datos de forma asincrónica.

Normalmente, arrastrar y colocar es una operación sincrónica. En resumen:

1.  El origen drop llama [**a DoDragDrop y**](/windows/win32/api/ole2/nf-ole2-dodragdrop) bloquea su subproceso principal hasta que se devuelve la función. Bloquear el subproceso principal normalmente bloquea el procesamiento de la interfaz de usuario.
2.  Después de llamar al método [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) del destino, el destino extrae los datos del objeto de datos en su subproceso principal. Este procedimiento normalmente bloquea el procesamiento de la interfaz de usuario del destino mientras dure el proceso de extracción.
3.  Una vez extraídos los datos, el destino devuelve la llamada [**IDropTarget::D rop,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) el sistema devuelve [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)y ambos subprocesos pueden continuar.

En resumen, la transferencia de datos sincrónica puede bloquear los subprocesos principales de ambas aplicaciones durante un período de tiempo significativo. En concreto, ambos subprocesos deben esperar mientras el destino extrae los datos. Para pequeñas cantidades de datos, el tiempo necesario para extraer datos es pequeño y la transferencia de datos sincrónica funciona bastante bien. Sin embargo, la extracción sincrónica de grandes cantidades de datos puede provocar retrasos largos e interferir con la interfaz de usuario de destino y origen.

La [**interfaz IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) es una interfaz opcional que puede implementar un objeto de datos. Proporciona al destino de colocación la capacidad de extraer datos del objeto de datos de forma asincrónica en un subproceso en segundo plano. Una vez que la extracción de datos se entrega al subproceso en segundo plano, los subprocesos principales de ambas aplicaciones pueden continuar.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Uso de IASyncOperation/IDataObjectAsyncCapability

> [!Note]  
> La interfaz se denominaba originalmente [**IAsyncOperation,**](/previous-versions//bb776309(v=vs.85))pero más adelante se cambió a [**IDataObjectAsyncCapability.**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) De lo contrario, las dos interfaces son idénticas.

 

El propósito de [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) es permitir que el origen y el destino de colocación negocien si los datos se pueden extraer de forma asincrónica. En el procedimiento siguiente se describe cómo el origen de colocación usa la interfaz :

1.  Cree un objeto de datos que exponga [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability.**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability)
2.  Llame [**a SetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) con *fDoOpAsync* establecido en **VARIANT \_ TRUE** para indicar que se admite una operación asincrónica.
3.  Después [**de que DoDragDrop vuelva,**](/windows/win32/api/ole2/nf-ole2-dodragdrop) llame a [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation):
    -   Si Se produce un error en [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) o devuelve **VARIANT \_ FALSE,** se ha realizado una transferencia de datos sincrónica normal y se ha finalizado el proceso de extracción de datos. El origen debe realizar cualquier limpieza necesaria y continuar.
    -   Si [**InOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) devuelve **VARIANT \_ TRUE**, los datos se extraen de forma asincrónica. EndOperation debe controlar las operaciones de [**limpieza.**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation)
4.  Liberar el objeto de datos.
5.  Una vez completada la transferencia de datos asincrónica, el objeto de datos normalmente notifica al origen a través de una interfaz privada.

En el procedimiento siguiente se describe [](/previous-versions//bb776309(v=vs.85))cómo el destino de colocación usa la interfaz / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) de IAsyncOperation para extraer datos de forma asincrónica:

1.  Cuando el sistema llama a [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop), llame a [**IDataObject::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y solicite una interfaz [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) (IID \_ IAsyncOperation/IID IDataObjectAsyncCapability) desde el objeto de \_ datos.
2.  Llame [**a GetAsyncMode.**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode) Si el método devuelve **VARIANT \_ TRUE**, el objeto de datos admite la extracción asincrónica de datos.
3.  Cree un subproceso independiente para controlar la extracción de datos y llame [**a StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation).
4.  Devuelve la [**llamada IDropTarget::D rop,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) como lo haría para una operación de transferencia de datos normal. [**DoDragDrop devolverá**](/windows/win32/api/ole2/nf-ole2-dodragdrop) y desbloqueará el origen de colocación. No llame a [**IDataObject::SetData para**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) indicar el resultado de una operación optimizada de movimiento o eliminación al pegar. Espere hasta que finalice la operación.
5.  Extraiga los datos del subproceso en segundo plano. El subproceso principal del destino está desbloqueado y es libre de continuar.
6.  Si la transferencia de datos era [una](#handling-optimized-move-operations) operación optimizada de movimiento o eliminación [al](#handling-delete-on-paste-operations) pegar, llame a [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para indicar el resultado.
7.  Notifique al objeto de datos que la extracción ha finalizado llamando [**a EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).

 

 
