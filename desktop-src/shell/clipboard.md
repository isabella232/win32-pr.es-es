---
description: Los formatos del portapapeles de Shell se usan para identificar el tipo de datos de Shell que se transfieren a través del portapapeles.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formatos del portapapeles de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808851"
---
# <a name="shell-clipboard-formats"></a>Formatos del portapapeles de Shell

Los formatos del portapapeles de Shell se usan para identificar el tipo de datos de Shell que se transfieren a través del portapapeles. La mayoría de los formatos del Portapapeles del shell identifican un tipo de datos, como una lista de nombres de archivo o punteros a listas de identificadores de elementos (PIDL). Sin embargo, se usan algunos formatos para la comunicación entre el origen y el destino. Pueden agilizar el proceso de transferencia de datos al admitir operaciones de shell como el movimiento y el [delete_on_paste](datascenarios.md) [optimizados](datascenarios.md) . Los datos de Shell siempre están contenidos en un [objeto de datos](dataobject.md) que usa una estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como una forma más general de caracterizar los datos. El miembro **cfFormat** de la estructura se establece en el formato del portapapeles para el elemento de datos determinado. Los demás miembros proporcionan información adicional, como el mecanismo de transferencia de datos. Los datos se encuentran en una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) adjunta.

> [!Note]  
> Los identificadores de formato del portapapeles estándar tienen el formato CF_ *XXX*. Un ejemplo común es CF_TEXT, que se usa para transferir datos de texto ANSI. Estos identificadores tienen valores predefinidos y se pueden utilizar directamente con estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . A excepción de [CF_HDROP](#cf_hdrop), los identificadores de formato de Shell no están predefinidos. Con la excepción de DragWindow, tienen el formato CFSTR_ *XXX*. Para diferenciar estos valores de los formatos predefinidos, a menudo se les denomina simplemente *formatos*. Sin embargo, a diferencia de los formatos predefinidos, se deben registrar tanto en el origen como en el destino antes de que se puedan usar para transferir datos. Para registrar un formato de Shell, incluya el archivo de encabezado ShlObj. h y pase el identificador de formato de CFSTR_ *XXX* a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Esta función devuelve un valor de formato de Portapapeles válido, que se puede usar como miembro **cfFormat** de una estructura **FORMATETC** .

 

Los formatos del portapapeles de Shell se organizan aquí en tres grupos, en función de cómo se utilicen.

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
    -   [CFSTR_SHELLURL (desusado)](#cfstr_shellurl-deprecated)
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

Estos formatos se utilizan para transferir uno o varios archivos u otros objetos de Shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Este formato del portapapeles se usa al transferir las ubicaciones de un grupo de archivos existentes. A diferencia de los demás formatos de Shell, está predefinido, por lo que no es necesario llamar a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **HGLOBAL** de la estructura apunta a una estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) como su miembro **HGLOBAL** .

El miembro **archivos pfile** de la estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene un desplazamiento a una matriz de caracteres doble terminada en **null** que contiene los nombres de archivo. Si va a extraer un formato de CF_HDROP de un objeto de datos, puede usar [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) para extraer nombres de archivo individuales del objeto de memoria global. Si va a crear un formato de CF_HDROP para colocarlo en un objeto de datos, deberá crear la matriz de nombres de archivo.

La matriz de nombres de archivo consta de una serie de cadenas, cada una de las cuales contiene la ruta de acceso completa de un archivo, incluido el carácter **nulo** de terminación. Se anexa un carácter **nulo** adicional a la cadena final para finalizar la matriz. Por ejemplo, si \\ se transfieren los archivos c:temp1.txt y c: \\temp2.txt, la matriz de caracteres tiene el siguiente aspecto:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> En este ejemplo, \\ se usa "0" para representar el carácter **nulo** , no los caracteres literales que se deben incluir.


Si el objeto se copió en el portapapeles como parte de una operación de arrastrar y colocar, el miembro **PT** de la estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene las coordenadas del punto en el que se quitó el objeto. Puede usar [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para extraer las coordenadas del cursor.

Si este formato está presente en un objeto de datos, un bucle de arrastre OLE simula [**WM_DROPFILES**](wm-dropfiles.md) funcionalidad con destinos de colocación que no son de OLE. Esto es importante si la aplicación es el origen de una operación de arrastrar y colocar en un sistema de Windows 3,1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Este identificador de formato se usa con el formato de [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) para transferir los datos como si fuera un archivo, independientemente de cómo se almacenen realmente. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que representa el contenido de un archivo. Normalmente, el archivo se representa como un objeto de flujo, lo que evita tener que colocar el contenido del archivo en la memoria. En ese caso, el miembro **tymed** de la estructura **STGMEDIUM** se establece en TYMED_ISTREAM y el archivo se representa mediante una interfaz [**ISTREAM**](/windows/win32/api/objidl/nn-objidl-istream) . El archivo también puede ser un objeto de almacenamiento o de memoria global (TYMED_ISTORAGE o TYMED_HGLOBAL). El formato de CFSTR_FILEDESCRIPTOR asociado contiene una estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada archivo que especifica el nombre y los atributos del archivo.

El destino trata los datos asociados a un formato de CFSTR_FILECONTENTS como si fuera un archivo. Cuando el destino llama a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extraer los datos, especifica un archivo determinado estableciendo el miembro **lIndex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en el índice de base cero de la estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) del archivo en el formato de [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) que lo acompaña. A continuación, el destino usa el puntero de interfaz devuelto o el identificador de memoria global para extraer los datos.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Este identificador de formato se usa con el formato [CFSTR_FILECONTENTS](#cfstr_filecontents) para transferir datos como un grupo de archivos. Estos dos formatos son la manera preferida de transferir objetos de Shell que no se almacenan como archivos de sistema de archivos. Por ejemplo, estos formatos se pueden usar para transferir un grupo de mensajes de correo electrónico como archivos individuales, aunque cada correo electrónico se almacena realmente como un bloque de datos en una base de datos. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una estructura [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) seguida de una matriz que contiene una estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada archivo del grupo. Para cada estructura de **FILEDESCRIPTOR** , hay un formato de CFSTR_FILECONTENTS independiente que incluye el contenido del archivo. Para identificar el formato de CFSTR_FILECONTENTS de un archivo determinado, establezca el valor **lIndex** de la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en el índice de base cero de la estructura **FILEDESCRIPTOR** del archivo.

El formato de CFSTR_FILEDESCRIPTOR se usa normalmente para transferir datos como si fuera un grupo de archivos, independientemente de cómo se almacenen realmente. Desde la perspectiva del destino, cada formato de CFSTR_FILECONTENTS representa un único archivo y se trata en consecuencia. Sin embargo, el origen puede almacenar los datos de la forma que elija. Aunque un formato de CSFTR_FILECONTENTS podría corresponder a un solo archivo, también podría representar los datos extraídos por el origen de una base de datos o un documento de texto.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Este identificador de formato se utiliza para transferir un solo archivo. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una sola cadena terminada en **null** que contiene la ruta de acceso completa del archivo. [CF_HDROP](#cf_hdrop)ha reemplazado este formato, pero se admite por compatibilidad con versiones anteriores de las aplicaciones de Windows 3,1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Este identificador de formato se usa cuando se cambia el nombre de un grupo de archivos en [CF_HDROP](#cf_hdrop) formato y se transfieren. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una matriz de caracteres doble terminada en **null**. Esta matriz contiene un nombre nuevo para cada archivo, en el mismo orden en que se muestran los archivos en el formato de CF_HDROP que lo acompaña. El formato de la matriz de caracteres es el mismo que el utilizado por CF_HDROP para enumerar los archivos transferidos.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Este identificador de formato se usa para transferir una ruta de acceso en un volumen montado. Es similar a [CF_HDROP](#cf_hdrop), pero contiene una sola ruta de acceso y puede controlar las cadenas de ruta de acceso más largas que podrían ser necesarias para representar una ruta de acceso cuando el volumen se monta en una carpeta. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una sola cadena terminada en **null** que contiene la ruta de acceso completa del archivo. La cadena de ruta de acceso debe terminar con un \\ carácter ' ', seguido del **valor null** final.

Antes de Windows 2000, los volúmenes solo se podían montar en Letras de unidad. Para Windows 2000 y sistemas posteriores con una unidad con formato NTFS, también puede montar volúmenes en carpetas vacías. Esta característica permite montar un volumen sin ocupar una letra de unidad. El volumen montado puede usar cualquier formato admitido actualmente, como FAT, FAT32, NTFS y CDFS.

Puede agregar páginas a la hoja de propiedades de las propiedades de la unidad implementando un controlador de la [hoja de propiedades](propsheet-handlers.md). Si el volumen se monta en una letra de unidad, el shell pasa información de la ruta de acceso al controlador con el formato de [CF_HDROP](#cf_hdrop) . Con Windows 2000 y sistemas posteriores, el formato de CF_HDROP se usa cuando un volumen se monta en una letra de unidad, al igual que con sistemas anteriores. Sin embargo, si se monta un volumen en una carpeta, se usa el identificador de formato [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) en lugar de CF_HDROP.

Si solo se usarán Letras de unidad para montar volúmenes, solo se utilizará [CF_HDROP](#cf_hdrop) y los controladores de hoja de propiedades existentes funcionarán como lo hacían con sistemas anteriores. Sin embargo, si desea que el controlador muestre una página para los volúmenes montados en carpetas y Letras de unidad, el controlador debe ser capaz de comprender los formatos CSFTR_MOUNTEDVOLUME y CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Este identificador de formato se usa al transferir las ubicaciones de uno o más objetos de espacio de nombres existentes. Se usa de forma muy similar a [CF_HDROP](#cf_hdrop), pero contiene PIDL en lugar de rutas de acceso del sistema de archivos. El uso de PIDL permite que el formato de CFSTR_SHELLIDLIST controle los objetos virtuales y los objetos del sistema de archivos. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de [**la estructura apunta a una**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) subestructura.

El miembro **aoffset** de la interfaz [**biocida**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) es una matriz que contiene los desplazamientos al principio de la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para cada PIDL que se va a transferir. Para extraer un PIDL determinado, determine primero su índice. A continuación, agregue el valor **aoffset** que corresponde a ese índice a la dirección de la **subestructura.**

El primer elemento de **aoffset** contiene un desplazamiento a la PIDL completa de una carpeta principal. Si esta PIDL está vacía, la carpeta principal es el escritorio. Cada uno de los elementos restantes de la matriz contiene un desplazamiento a uno de los PIDL que se van a transferir. Todos estos PIDL son relativos al PIDL de la carpeta principal.

Las dos macros siguientes se pueden usar para recuperar PIDL [**de una**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) subestructura. La primera toma un puntero a la estructura y recupera el PIDL de la carpeta principal. La segunda toma un puntero a la estructura y recupera uno de los otros PIDL, identificado por su índice basado en cero.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> El valor devuelto por estas macros es un puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) de PIDL. Dado que estas estructuras tienen una longitud diferente, debe determinar el final de la estructura recorriendo cada una de las estructuras de [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de la estructura **ITEMIDLIST** hasta llegar al **valor null** de dos bytes que marca el final.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Este identificador de formato se usa con formatos como [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)y [CFSTR_FILECONTENTS](#cfstr_filecontents) para especificar la posición de un grupo de objetos después de una transferencia. Los datos están formados por una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una matriz de estructuras de [**puntos**](/previous-versions//dd162805(v=vs.85)) . La primera estructura especifica las coordenadas de la pantalla, en píxeles, de la esquina superior izquierda del rectángulo que incluye el grupo. El resto de las estructuras especifican las ubicaciones de los objetos individuales en relación con la posición del grupo. Deben estar en el mismo orden que se usa para enumerar los objetos en el formato asociado.

## <a name="formats-for-transferring-virtual-objects"></a>Formatos para transferir objetos virtuales

El formato de CFSTR_SHELLIDLIST se puede utilizar para transferir los objetos virtuales y del sistema de archivos. Sin embargo, también hay varios formatos especializados para transferir determinados tipos de objetos virtuales.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (desusado)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Este identificador de formato se usa al transferir recursos de red, como un dominio o un servidor. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una estructura [**NRESARRAY**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) . El miembro **NR** de esa estructura indica una estructura [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) cuyo miembro **lpRemoteName** contiene una cadena terminada en **null** que identifica el recurso de red. A continuación, el destino de colocación puede usar los datos con cualquiera de las funciones de la API de [redes de Windows (WNet)](../wnet/windows-networking-wnet-.md) , como [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona), para realizar operaciones de red en el objeto.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Este identificador de formato se usa al transferir los nombres descriptivos de las impresoras. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una cadena en el mismo formato que el utilizado con [CF_HDROP](#cf_hdrop). Sin embargo, el miembro **archivos pfile** de la estructura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene uno o más nombres descriptivos de las impresoras en lugar de rutas de acceso de archivo.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Este identificador de formato reemplaza [CFSTR_SHELLURL (desusado)](#cfstr_shellurl-deprecated). Si desea que la aplicación manipule las direcciones URL del portapapeles, use CFSTR_INETURL en lugar de CFSTR_SHELLURL (en desuso). Este formato proporciona la mejor representación del portapapeles de una sola dirección URL. Si no se define Unicode, la aplicación recupera la versión CF_TEXT/CFSTR_SHELLURL de la dirección URL. Si se define Unicode, la aplicación recupera la versión CF_UNICODE de la dirección URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (desusado)

> [!Note]  
> Este identificador de formato ha quedado en desuso; en su lugar, use CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formatos para la comunicación entre el origen y el destino

Estos identificadores de formato permiten la comunicación entre el origen y el destino. Los formatos acompañan a los datos y proporcionan a las aplicaciones un mayor grado de control sobre las operaciones de arrastrar y colocar que afectan a los objetos de Shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Un objeto de datos usa este identificador de formato para indicar si está en un bucle de arrastrar y colocar. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a un valor **DWORD** . Si el valor **DWORD** es distinto de cero, el objeto de datos se encuentra dentro de un bucle de arrastrar y colocar. Si el valor se establece en cero, el objeto de datos no se encuentra dentro de un bucle de arrastrar y colocar.

Algunos destinos de colocación pueden llamar a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) e intentar extraer datos mientras el objeto todavía está dentro del bucle de arrastrar y colocar. La representación completa del objeto para cada uno de estos casos podría provocar que se detenga el cursor de arrastre. Si el objeto de datos admite [CFSTR_INDRAGLOOP](#cfstr_indragloop), el destino puede usar en su lugar ese formato para comprobar el estado del bucle de arrastrar y colocar y evitar la representación intensiva de memoria del objeto hasta que realmente se quite. Los formatos que consumen mucha memoria para representarse deben seguir incluidos en el enumerador [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y en las llamadas a [**IDataObject:: QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata). Si el objeto de datos no establece CFSTR_INDRAGLOOP, debe actuar como si el valor se establece en cero.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Versión 5,0.](versions.md) Este identificador de formato permite a un origen de colocación llamar al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos para determinar el resultado de una transferencia de datos de Shell. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a un DWORD que contiene un valor de [**DROPEFFECT**](../com/dropeffect-constants.md) .

El identificador de formato de [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) estaba diseñado para permitir que el destino indique al objeto de datos qué operación tuvo lugar realmente. Sin embargo, el shell utiliza [movimientos optimizados](datascenarios.md) para objetos del sistema de archivos siempre que sea posible. En ese caso, el Shell establece normalmente el valor CFSTR_PERFORMEDDROPEFFECT en DROPEFFECT_NONE, para indicar al objeto de datos que se han eliminado los datos originales. Por lo tanto, el origen no puede usar el valor CFSTR_PERFORMEDDROPEFFECT para determinar la operación que ha tenido lugar. Aunque la mayoría de los orígenes no necesitan esta información, hay algunas excepciones. Por ejemplo, aunque los movimientos optimizados eliminan la necesidad de que un origen elimine los datos, es posible que el origen aún tenga que actualizar una base de datos relacionada para indicar que los archivos se han trasladado o copiado.

Si un origen necesita saber qué operación tuvo lugar, puede llamar al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos y solicitar el formato de CFSTR_LOGICALPERFORMEDDROPEFFECT. Este formato refleja básicamente lo que sucede desde el punto de vista del usuario una vez completada la operación. Si se crea un nuevo archivo y se elimina el archivo original, el usuario ve una operación de movimiento y el valor de los datos del formato se establece en DROPEFFECT_MOVE. Si el archivo original todavía existe, el usuario verá una operación de copia y el valor de los datos del formato se establecerá en DROPEFFECT_COPY. Si se ha creado un vínculo, el valor de los datos del formato será DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

El destino utiliza este identificador de formato para informar al objeto de datos, a través de su método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) , que la operación de eliminación en pegado se realizó correctamente. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a un **DWORD** que contiene un valor de [**DROPEFFECT**](../com/dropeffect-constants.md) . Este formato se utiliza para notificar al objeto de datos que debe completar la operación de cortar y eliminar los datos originales, si es necesario. Para obtener más información, consulte [operaciones de eliminación y pegado](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

El destino utiliza este identificador de formato para informar al objeto de datos a través de su método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del resultado de una transferencia de datos. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a una **DWORD** establecida en el valor [**DROPEFFECT**](../com/dropeffect-constants.md) adecuado, normalmente DROPEFFECT_MOVE o DROPEFFECT_COPY.

Este formato se utiliza normalmente cuando el resultado de una operación puede ser movimiento o copia, como en una operación de [movimiento o eliminación optimizada](datascenarios.md) . Proporciona un método confiable para que el destino indique al objeto de datos lo que ha sucedido realmente. Se presentó porque el valor de *pdwEffect* devuelto por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) no indicaba de forma confiable qué operación había tenido lugar. El formato de [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) es la forma confiable de indicar que se ha producido un movimiento no optimizado.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

El origen usa este identificador de formato para especificar si su método preferido de transferencia de datos es Move o Copy. Un destino de colocación solicita este formato llamando al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a un valor **DWORD** . Este valor se establece en DROPEFFECT_MOVE si se prefiere una operación de movimiento o DROPEFFECT_COPY si se prefiere una operación de copia.

Esta característica se utiliza cuando un origen puede admitir una operación de movimiento o copia. Utiliza el formato de [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) para comunicar sus preferencias al destino. Dado que el destino no está obligado a respetar la solicitud, el destino debe llamar al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con un formato de [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) para indicar al objeto de datos qué operación se realizó realmente.

Con una operación de [eliminar al pegar](datascenarios.md) , se usa el formato de CFSTR_PREFERREDDROPFORMAT para indicar al destino si el origen hizo un corte o una copia. Con una operación de arrastrar y colocar, puede usar CFSTR_PREFERREDDROPFORMAT para especificar la acción del shell. Si este formato no está presente, el shell realiza una acción predeterminada basada en el contexto. Por ejemplo, si un usuario arrastra un archivo de un volumen y lo coloca en otro volumen, la acción predeterminada del shell es copiar el archivo. Al incluir un CFSTR_PREFERREDDROPFORMAT formato en el objeto de datos, puede invalidar la acción predeterminada y indicar explícitamente al shell que copie, mueva o vincule el archivo. Si el usuario elige arrastrar con el botón derecho, CFSTR_PREFERREDDROPFORMAT especifica el comando predeterminado en el menú contextual de [arrastrar y colocar](context-menu-handlers.md) . El usuario sigue siendo gratuito para elegir otros comandos en el menú.

Antes de Microsoft Internet Explorer 4,0, una aplicación indica que se transfieren los tipos de archivo de acceso directo estableciendo FD_LINKUI en el miembro **dwFlags** de la estructura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Los destinos tenían que usar una llamada potencialmente lenta a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para averiguar si se ha establecido la marca de FD_LINKUI. Ahora, la mejor manera de indicar que los métodos abreviados se están transfiriendo es usar el formato CFSTR_PREFERREDDROPEFFECT establecido en DROPEFFECT_LINK. Sin embargo, para la compatibilidad con versiones anteriores de sistemas anteriores, los orígenes deberían seguir configurando la marca de FD_LINKUI.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Un destino utiliza este identificador de formato para proporcionar su CLSID al origen. Los datos son una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta al GUID de CLSID del destino de colocación.

Este formato se usa principalmente para permitir la eliminación de objetos arrastrándolos a la papelera de reciclaje. Cuando se coloca un objeto en la papelera de reciclaje, se llama al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del origen con un formato CFSTR_TARGETCLSID establecido en el CLSID de la papelera de reciclaje (CLSID_RecycleBin). Después, el origen puede eliminar el objeto original.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Windows Internet Explorer y el shell de Windows usan este identificador de formato para proporcionar un mecanismo a través del cual bloquear o solicitar las operaciones de arrastrar y colocar que se originan en Internet Explorer junto con la marca de [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) .

El origen de una operación de arrastrar y colocar agrega **CFSTR_UNTRUSTEDDRAGDROP** para especificar que el objeto de datos puede contener datos no confiables. Los datos se representan mediante una estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contiene un objeto de memoria global. El miembro **hGlobal** de la estructura apunta a **un valor DWORD** establecido en una marca de [**acción de dirección URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) adecuada para que se produzca una comprobación de directiva a través del método [**IInternetSecurityManager::P rocessurlaction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) , mediante el uso de la marca [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) .

### <a name="dragwindow"></a>DragWindow

Este formato se usa en una operación de arrastrar y colocar para identificar la imagen de arrastre (ventana) de un objeto de modo que su información visual se pueda actualizar dinámicamente. Cuando se arrastra un objeto sobre un destino de colocación, una aplicación actualiza su estructura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) en respuesta al método [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) o [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . **DROPDESCRIPTION** se actualiza con un nuevo valor de [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica la decoración que se va a aplicar al visual de la ventana de arrastre. por ejemplo, indica que el archivo se está copiando en lugar de moverse o que el objeto no se puede quitar a esa ubicación. Sin embargo, hasta que el objeto recibe un mensaje de [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) , no se actualizan los objetos visuales. Este formato proporciona el **hWnd** de la ventana de arrastre del destinatario al remitente del mensaje de **DDWM_UPDATEWINDOW** .

Los datos del portapapeles son del tipo [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). Es una representación **DWORD** de un **hWnd**. Los datos se pueden pasar a la función **ULongToHandle** , definida en Basetsd. h, para proporcionar un **hWnd** de 64 bits para su uso en Windows de 64 bits.

Este formato no requiere la inclusión de ShlObj. h.

 

 
