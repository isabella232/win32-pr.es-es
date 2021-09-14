---
description: Los formatos del Portapapeles de Shell se usan para identificar el tipo de datos de Shell que se transfieren a través del Portapapeles.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formatos del Portapapeles de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363171"
---
# <a name="shell-clipboard-formats"></a>Formatos del Portapapeles de Shell

Los formatos del Portapapeles de Shell se usan para identificar el tipo de datos de Shell que se transfieren a través del Portapapeles. La mayoría de los formatos del Portapapeles de Shell identifican un tipo de datos, como una lista de nombres de archivo o punteros a listas de identificadores de elementos (PIDL). Sin embargo, algunos formatos se usan para la comunicación entre el origen y el destino. Pueden acelerar el proceso de transferencia de datos si admiten operaciones de Shell como el movimiento [optimizado](datascenarios.md) [y delete_on_paste](datascenarios.md). Los datos del shell siempre se incluyen en un [objeto de datos que](dataobject.md) usa una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como una manera más general de caracterizar los datos. El miembro **cfFormat de la** estructura se establece en el formato del Portapapeles para el elemento de datos concreto. Los demás miembros proporcionan información adicional, como el mecanismo de transferencia de datos. Los datos están contenidos en una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que lo acompaña.

> [!Note]  
> Los identificadores de formato estándar del Portapapeles tienen el CF_ *XXX*. Un ejemplo común es CF_TEXT, que se usa para transferir datos de texto ANSI. Estos identificadores tienen valores predefinidos y se pueden usar directamente con [**estructuras FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) A excepción de [CF_HDROP](#cf_hdrop), los identificadores de formato de shell no están predefinidos. A excepción de DragWindow, tienen el formato CFSTR_ *XXX*. Para diferenciar estos valores de los formatos predefinidos, a menudo se denominan *formatos simplemente*. Sin embargo, a diferencia de los formatos predefinidos, el origen y el destino deben registrar los formatos para poder transferir datos. Para registrar un formato de Shell, incluya el archivo de encabezado Shlobj.h y pase el identificador CFSTR_ *formato XXX* a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Esta función devuelve un valor de formato válido del Portapapeles, que se puede usar como miembro **cfFormat** de **una estructura FORMATETC.**

 

Los formatos del Portapapeles de Shell se organizan aquí en tres grupos, en función de cómo se usan.

-   [Formatos para transferir objetos del sistema de archivos](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formatos para transferir objetos virtuales](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (en desuso)](#cfstr_shellurl-deprecated)
-   [Formatos para la comunicación entre el origen y el destino](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formatos para transferir objetos del sistema de archivos

Estos formatos se usan para transferir uno o varios archivos u otros objetos de Shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Este formato del Portapapeles se usa al transferir las ubicaciones de un grupo de archivos existentes. A diferencia de los otros formatos de Shell, está predefinido, por lo que no es necesario llamar a [RegisterClipboardFormat.](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a una [**estructura DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) como **su miembro hGlobal.**

El **miembro pFiles** de la [**estructura DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene un desplazamiento a una matriz de caracteres terminada en null doble que contiene los nombres de archivo.  Si va a extraer un formato CF_HDROP de un objeto de datos, puede usar [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) para extraer nombres de archivo individuales del objeto de memoria global. Si va a crear un formato CF_HDROP para colocarlo en un objeto de datos, deberá construir la matriz de nombres de archivo.

La matriz de nombres de archivo consta de una serie de cadenas, cada una de las cuales contiene la ruta de acceso completa de un archivo, incluido el carácter **NULL de** terminación. Se anexa **un carácter null** adicional a la cadena final para finalizar la matriz. Por ejemplo, si los archivos c:temp1.txt y c:temp2.txt se transfieren, la matriz de caracteres \\ \\ tiene el siguiente aspecto:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> En este ejemplo, se usa '0' para representar el carácter \\ **nulo,** no los caracteres literales que se deben incluir.


Si el objeto se copió en el Portapapeles como parte de una operación de arrastrar y colocar, el miembro **pt** de la estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene las coordenadas del punto donde se ha eliminado el objeto. Puede usar [**DragQueryPoint para**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) extraer las coordenadas del cursor.

Si este formato está presente en un objeto de datos, un bucle de arrastre OLE [**simula**](wm-dropfiles.md) WM_DROPFILES funcionalidad con destinos de colocación que no son OLE. Esto es importante si la aplicación es el origen de una operación de arrastrar y colocar en un Windows 3.1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Este identificador de formato se usa con el [formato CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) para transferir datos como si fuera un archivo, independientemente de cómo se almacene realmente. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que representa el contenido de un archivo. Normalmente, el archivo se representa como un objeto de secuencia, lo que evita tener que colocar el contenido del archivo en memoria. En ese caso, el miembro **tymed** de la estructura **STGMEDIUM** se establece en TYMED_ISTREAM y el archivo se representa mediante una [**interfaz IStream.**](/windows/win32/api/objidl/nn-objidl-istream) El archivo también puede ser un objeto de almacenamiento o de memoria global (TYMED_ISTORAGE o TYMED_HGLOBAL). El formato CFSTR_FILEDESCRIPTOR asociado contiene una [**estructura FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada archivo que especifica el nombre y los atributos del archivo.

El destino trata los datos asociados con un formato CFSTR_FILECONTENTS como si fuera un archivo. Cuando el destino llama a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extraer los datos, especifica un archivo determinado estableciendo el **miembro lindex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en el índice de base cero de la estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) del archivo en el formato [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) adjunto. A continuación, el destino usa el puntero de interfaz devuelto o el identificador de memoria global para extraer los datos.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Este identificador de formato se usa con [el CFSTR_FILECONTENTS](#cfstr_filecontents) para transferir datos como un grupo de archivos. Estos dos formatos son la manera preferida de transferir objetos de Shell que no se almacenan como archivos del sistema de archivos. Por ejemplo, estos formatos se pueden usar para transferir un grupo de mensajes de correo electrónico como archivos individuales, aunque cada correo electrónico se almacene realmente como un bloque de datos en una base de datos. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una estructura [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) seguida de una matriz que contiene una estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada archivo del grupo. Para cada **estructura FILEDESCRIPTOR,** hay un formato CFSTR_FILECONTENTS que contiene el contenido del archivo. Para identificar el formato de CFSTR_FILECONTENTS de un archivo determinado, establezca el valor **lIndex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en el índice de base cero de la estructura **FILEDESCRIPTOR** del archivo.

El CFSTR_FILEDESCRIPTOR se usa normalmente para transferir datos como si fuera un grupo de archivos, independientemente de cómo se almacenen realmente. Desde la perspectiva del destino, cada formato CFSTR_FILECONTENTS representa un único archivo y se trata en consecuencia. Sin embargo, el origen puede almacenar los datos de la manera que elija. Aunque un CSFTR_FILECONTENTS puede corresponder a un único archivo, también podría, por ejemplo, representar los datos extraídos por el origen de una base de datos o un documento de texto.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Este identificador de formato se usa para transferir un único archivo. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una única cadena terminada en **NULL** que contiene la ruta de acceso completa del archivo. Este formato se ha reemplazado [por](#cf_hdrop)CF_HDROP , pero se admite por compatibilidad con versiones anteriores con Windows 3.1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Este identificador de formato se usa cuando se cambia el nombre de un grupo de archivos [en CF_HDROP](#cf_hdrop) se cambia el nombre y se transfiere. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una matriz **de caracteres** terminada en null doble. Esta matriz contiene un nuevo nombre para cada archivo, en el mismo orden en que los archivos aparecen en el formato CF_HDROP archivo. El formato de la matriz de caracteres es el mismo que el utilizado por CF_HDROP enumerar los archivos transferidos.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Este identificador de formato se usa para transferir una ruta de acceso en un volumen montado. Es similar a [CF_HDROP](#cf_hdrop), pero solo contiene una ruta de acceso única y puede controlar las cadenas de ruta de acceso más largas que podrían ser necesarias para representar una ruta de acceso cuando el volumen se monta en una carpeta. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una única cadena terminada en **NULL** que contiene la ruta de acceso de archivo completa. La cadena de ruta de acceso debe terminar con un carácter \\ '', seguido del valor **NULL final.**

Antes de Windows 2000, los volúmenes solo se podían montar en letras de unidad. Para Windows sistemas 2000 y posteriores con una unidad con formato NTFS, también puede montar volúmenes en carpetas vacías. Esta característica permite montar un volumen sin tener que tomar una letra de unidad. El volumen montado puede usar cualquier formato admitido actualmente, como FAT, FAT32, NTFS y CDFS.

Puede agregar páginas a una hoja de propiedades Propiedades de unidad implementando un controlador [de hoja de propiedades](propsheet-handlers.md). Si el volumen se monta en una letra de unidad, el Shell pasa la información de ruta de acceso al controlador con [el CF_HDROP](#cf_hdrop) formato. Con Windows 2000 y versiones posteriores, se usa el formato CF_HDROP cuando un volumen se monta en una letra de unidad, igual que con sistemas anteriores. Sin embargo, si un volumen se monta en una carpeta, se [usa](#cfstr_mountedvolume) CFSTR_MOUNTEDVOLUME identificador de formato en lugar de CF_HDROP.

Si solo se usarán letras de [](#cf_hdrop) unidad para montar volúmenes, solo se usarán CF_HDROP y los controladores de hoja de propiedades existentes funcionarán como lo hacían con sistemas anteriores. Sin embargo, si desea que el controlador muestre una página para los volúmenes montados en carpetas, así como las letras de unidad, el controlador debe ser capaz de comprender los formatos CSFTR_MOUNTEDVOLUME y CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Este identificador de formato se usa al transferir las ubicaciones de uno o varios objetos de espacio de nombres existentes. Se usa de la misma manera que [CF_HDROP](#cf_hdrop), pero contiene PIDL en lugar de rutas de acceso del sistema de archivos. El uso de PIDL permite que CFSTR_SHELLIDLIST controle los objetos virtuales, así como los objetos del sistema de archivos. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a una [**estructura CIDA.**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida)

El **miembro aoffset** de la estructura CIDA es una [**matriz**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) que contiene desplazamientos al principio de la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para cada PIDL que se transfiere. Para extraer un PIDL determinado, primero determine su índice. A continuación, **agregue el valor aoffset** que corresponde a ese índice a la dirección de la **estructura CIDA.**

El primer elemento de **aoffset** contiene un desplazamiento al PIDL completo de una carpeta primaria. Si este PIDL está vacío, la carpeta primaria es el escritorio. Cada uno de los elementos restantes de la matriz contiene un desplazamiento a uno de los PIDL que se transferirán. Todos estos PIDL son relativos al PIDL de la carpeta primaria.

Las dos macros siguientes se pueden usar para recuperar los PIDL de una [**estructura CIDA.**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) El primero toma un puntero a la estructura y recupera el PIDL de la carpeta primaria. El segundo toma un puntero a la estructura y recupera una de las otras PIDL, identificadas por su índice de base cero.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> El valor devuelto por estas macros es un puntero a la estructura [**ITEMIDLIST del PIDL.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Dado que estas estructuras varían de longitud, debe determinar el final de la estructura recorrindo cada una de las estructuras DE LA estructura **ITEMIDLIST** [**HASTA**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) llegar al valor **NULL** de dos bytes que marca el final.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Este identificador de formato se usa con formatos [como CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)y [CFSTR_FILECONTENTS](#cfstr_filecontents) para especificar la posición de un grupo de objetos después de una transferencia. Los datos constan de una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una matriz de [**estructuras POINT.**](/previous-versions//dd162805(v=vs.85)) La primera estructura especifica las coordenadas de pantalla, en píxeles, de la esquina superior izquierda del rectángulo que incluye el grupo. El resto de las estructuras especifican las ubicaciones de los objetos individuales en relación con la posición del grupo. Deben estar en el mismo orden que el utilizado para enumerar los objetos en el formato asociado.

## <a name="formats-for-transferring-virtual-objects"></a>Formatos para transferir objetos virtuales

El CFSTR_SHELLIDLIST se puede usar para transferir objetos virtuales y del sistema de archivos. Sin embargo, también hay varios formatos especializados para transferir determinados tipos de objetos virtuales.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (en desuso)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Este identificador de formato se usa al transferir recursos de red, como un dominio o un servidor. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a una [**estructura NRESARRAY.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) El **miembro nr** de esa estructura indica una estructura [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) cuyo **miembro lpRemoteName** contiene una cadena terminada en **NULL** que identifica el recurso de red. Después, el destino de colocación puede usar los datos con cualquiera de las funciones de api de [Windows Networking (WNet),](../wnet/windows-networking-wnet-.md) como [**WNetAddConnection,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)para realizar operaciones de red en el objeto .

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Este identificador de formato se usa al transferir los nombres descriptivos de las impresoras. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a una cadena en el mismo formato que se usa [con CF_HDROP](#cf_hdrop). Sin embargo, **el miembro pFiles** de la [**estructura DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene uno o varios nombres descriptivos de impresoras en lugar de rutas de acceso de archivo.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Este identificador de formato reemplaza [CFSTR_SHELLURL (en desuso).](#cfstr_shellurl-deprecated) Si desea que la aplicación manipule las direcciones URL del Portapapeles, use CFSTR_INETURL en lugar de CFSTR_SHELLURL (en desuso). Este formato proporciona la mejor representación del Portapapeles de una sola dirección URL. Si no se define UNICODE, la aplicación recupera la CF_TEXT/CFSTR_SHELLURL de la dirección URL. Si se define UNICODE, la aplicación recupera la CF_UNICODE de la dirección URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (en desuso)

> [!Note]  
> Este identificador de formato está en desuso; use CFSTR_INETURL en su lugar.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formatos para la comunicación entre el origen y el destino

Estos identificadores de formato permiten la comunicación entre el origen y el destino. Los formatos acompañan a los datos y dan a las aplicaciones un mayor grado de control sobre las operaciones de mover, copiar, pegar o arrastrar y colocar que implican objetos de Shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Un objeto de datos usa este identificador de formato para indicar si está en un bucle de arrastrar y colocar. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a un **valor DWORD.** Si el **valor DWORD** es distinto de cero, el objeto de datos se encuentra dentro de un bucle de arrastrar y colocar. Si el valor se establece en cero, el objeto de datos no está dentro de un bucle de arrastrar y colocar.

Algunos destinos de colocación pueden llamar [**a IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) e intentar extraer datos mientras el objeto todavía está dentro del bucle de arrastrar y colocar. La representación completa del objeto para cada aparición de este tipo podría hacer que el cursor de arrastre se detendría. Si el objeto de datos admite [CFSTR_INDRAGLOOP](#cfstr_indragloop), el destino puede usar en su lugar ese formato para comprobar el estado del bucle de arrastrar y colocar y evitar la representación intensiva de memoria del objeto hasta que se coloque realmente. Los formatos que consumen mucha memoria para representar todavía deben incluirse en el enumerador [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y en las llamadas a [**IDataObject::QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata). Si el objeto de datos no CFSTR_INDRAGLOOP, debe actuar como si el valor se hubiera establecido en cero.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Versión 5.0.](versions.md) Este identificador de formato permite que un origen de colocación llame al método [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos para determinar el resultado de una transferencia de datos de Shell. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a un DWORD que contiene un [**valor DROPEFFECT.**](../com/dropeffect-constants.md)

El [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) de formato estaba pensado para permitir que el destino indicara al objeto de datos qué operación tuvo lugar realmente. Sin embargo, el Shell usa [movimientos optimizados para](datascenarios.md) objetos del sistema de archivos siempre que sea posible. En ese caso, el Shell normalmente establece el valor de CFSTR_PERFORMEDDROPEFFECT en DROPEFFECT_NONE, para indicar al objeto de datos que se han eliminado los datos originales. Por lo tanto, el origen no puede usar el CFSTR_PERFORMEDDROPEFFECT para determinar qué operación ha tenido lugar. Aunque la mayoría de los orígenes no necesitan esta información, hay algunas excepciones. Por ejemplo, aunque los movimientos optimizados eliminan la necesidad de que un origen elimine los datos, es posible que el origen tenga que actualizar una base de datos relacionada para indicar que los archivos se han movido o copiado.

Si un origen necesita saber qué operación se ha llevado a cabo, puede llamar al método [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos y solicitar CFSTR_LOGICALPERFORMEDDROPEFFECT formato. Este formato refleja básicamente lo que sucede desde el punto de vista del usuario una vez completada la operación. Si se crea un nuevo archivo y se elimina el archivo original, el usuario ve una operación de movimiento y el valor de datos del formato se establece en DROPEFFECT_MOVE. Si el archivo original sigue ahí, el usuario ve una operación de copia y el valor de datos del formato se establece en DROPEFFECT_COPY. Si se creó un vínculo, el valor de los datos del formato se DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

El destino usa este identificador de formato para informar al objeto de datos, a través de su método [**IDataObject::SetData,**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de que una operación de eliminación y pegado se ha hecho correctamente. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a un **DWORD** que contiene un [**valor DROPEFFECT.**](../com/dropeffect-constants.md) Este formato se usa para notificar al objeto de datos que debe completar la operación de corte y eliminar los datos originales, si es necesario. Para obtener más información, [vea Operaciones de eliminación y pegado.](datascenarios.md)

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

El destino usa este identificador de formato para informar al objeto de datos a través de su [**método IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del resultado de una transferencia de datos. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a un **DWORD** establecido en el valor [**DROPEFFECT**](../com/dropeffect-constants.md) adecuado, normalmente DROPEFFECT_MOVE o DROPEFFECT_COPY.

Este formato se usa normalmente cuando el resultado de una operación puede [](datascenarios.md) ser mover o copiar, como en una operación de movimiento optimizada o de eliminación y pegado. Proporciona una manera confiable para que el destino le diga al objeto de datos lo que realmente ha ocurrido. Se introdujo porque el valor de *pdwEffect* devuelto por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) no indicaba de forma confiable qué operación se había realizado. El [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) es la manera confiable de indicar que se ha realizado un movimiento sin optimizar.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

El origen usa este identificador de formato para especificar si su método preferido de transferencia de datos es mover o copiar. Un destino drop solicita este formato llamando al método [**IDataObject::GetData del**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) objeto de datos. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta a un **valor DWORD.** Este valor se establece en DROPEFFECT_MOVE si se prefiere una operación de movimiento o DROPEFFECT_COPY si se prefiere una operación de copia.

Esta característica se usa cuando un origen puede admitir una operación de movimiento o copia. Usa el formato [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) para comunicar su preferencia al destino. Dado que el destino no está obligado a respetar la solicitud, el destino debe llamar al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con un formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) para decir al objeto de datos qué operación se realizó realmente.

Con una [operación de](datascenarios.md) eliminación y pegado, el formato CFSTR_PREFERREDDROPFORMAT se usa para decir al destino si el origen ha hecho una operación de cortar o copiar. Con una operación de arrastrar y colocar, puede usar CFSTR_PREFERREDDROPFORMAT para especificar la acción del shell. Si este formato no está presente, el Shell realiza una acción predeterminada, en función del contexto. Por ejemplo, si un usuario arrastra un archivo de un volumen y lo coloca en otro volumen, la acción predeterminada del Shell es copiar el archivo. Al incluir un CFSTR_PREFERREDDROPFORMAT en el objeto de datos, puede invalidar la acción predeterminada e indir explícitamente al Shell que copie, mueva o vincule el archivo. Si el usuario elige arrastrar con el botón derecho, CFSTR_PREFERREDDROPFORMAT especifica el comando predeterminado en el menú contextual de arrastrar [y](context-menu-handlers.md) colocar. El usuario sigue teniendo la libertad de elegir otros comandos en el menú.

Antes de que Microsoft Internet Explorer 4.0, una aplicación indicara que estaba transfiriendo tipos de archivo de acceso directo estableciendo FD_LINKUI en el miembro **dwFlags** de la estructura [**FILEDESCRIPTOR.**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) A continuación, los destinos tenían que usar una llamada potencialmente lenta a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para averiguar si se FD_LINKUI marca de destino. Ahora, la manera preferida de indicar que se transfieren accesos directos es usar el formato CFSTR_PREFERREDDROPEFFECT establecido en DROPEFFECT_LINK. Sin embargo, para la compatibilidad con versiones anteriores con sistemas anteriores, los orígenes deben establecer la FD_LINKUI anterior.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Un destino usa este identificador de formato para proporcionar su CLSID al origen. Los datos son una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal de la** estructura apunta al GUID de CLSID del destino de colocación.

Este formato se usa principalmente para permitir que los objetos se eliminen arrastrándolos al papelera de reciclaje. Cuando se coloca un objeto en el papelera de reciclaje, se llama al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con un formato CFSTR_TARGETCLSID establecido en el CLSID (CLSID_RecycleBin) de papelera de reciclaje. A continuación, el origen puede eliminar el objeto original.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Windows Internet Explorer y el Shell de Windows usan este identificador de formato para proporcionar un mecanismo a través del cual bloquear o solicitar operaciones de arrastrar y colocar que se originen en Internet Explorer junto con la [**marca URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85))

**CFSTR_UNTRUSTEDDRAGDROP** agrega el origen de una operación de arrastrar y colocar para especificar que el objeto de datos puede contener datos no confiables. Los datos se representan mediante una [**estructura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a un **DWORD** establecido en una marca de acción de dirección [**URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) adecuada para provocar una comprobación de directiva a través del método [**IInternetSecurityManager::P rocessUrlAction,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) mediante la marca [**PUAF_ENFORCERESTRICTED.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85))

### <a name="dragwindow"></a>DragWindow

Este formato se usa en una operación de arrastrar y colocar para identificar la imagen de arrastre (ventana) de un objeto para que su información visual se pueda actualizar dinámicamente. Cuando se arrastra un objeto sobre un destino de colocación, una aplicación actualiza su estructura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) en respuesta al método [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) [**o IDropSource::GiveFeedback.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) **DROPDESCRIPTION** se actualiza con un nuevo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica la decoración que se va a aplicar al objeto visual de la ventana de arrastre. Por ejemplo, una indicación de que el archivo se está copiando en lugar de moverse o que el objeto no se puede eliminar en esa ubicación. Sin embargo, hasta que el [**objeto recibe DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) mensaje, los objetos visuales no se actualizan. Este formato proporciona el **HWND de** la ventana de arrastre del destinatario al remitente del **DDWM_UPDATEWINDOW** mensaje.

Los datos del Portapapeles son de [**tipo TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). Es una representación **DWORD** de un **HWND.** Los datos se pueden pasar a la función **ULongToHandle,** definida en Basetsd.h, para proporcionar un **HWND** de 64 bits para su uso en Windows de 64 bits.

Este formato no requiere la inclusión de Shlobj.h.

 

 
