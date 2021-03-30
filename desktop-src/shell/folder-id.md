---
description: Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtener el identificador de una carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997733"
---
# <a name="getting-a-folders-id"></a>Obtener el identificador de una carpeta

Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo. Esto significa obtener su puntero a una lista de identificadores de elemento (PIDL) o, en el caso de objetos del sistema de archivos, su ruta de acceso. En esta sección se describen dos de las formas más sencillas de obtener los identificadores de objeto.

Para un enfoque más eficaz que funcione con cualquier carpeta, use la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Vea obtener [información sobre el contenido de una carpeta](folder-info.md) para obtener más detalles.

-   [Cuadro de diálogo OpenFiles](#the-openfiles-dialog-box)
-   [Cuadro de diálogo SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Carpetas especiales y CSIDLs](#special-folders-and-csidls)
-   [Un ejemplo sencillo de cómo usar CSIDLs y SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Cuadro de diálogo OpenFiles

Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede usar la interfaz [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) . Al llamar a esta interfaz con la marca de **FOS \_ PICKFOLDERS** , se inicia el cuadro de diálogo de [abrir archivos](../dlgbox/open-and-save-as-dialog-boxes.md) comunes en el modo "seleccionar carpetas".

En Windows Vista y versiones posteriores, esta es la manera recomendada para elegir carpetas.

## <a name="the-shbrowseforfolder-dialog-box"></a>Cuadro de diálogo SHBrowseForFolder

Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede simplemente invocar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Al llamar a esta función, se inicia un cuadro de diálogo con una interfaz de usuario que funciona como los cuadros de diálogo comunes [abrir o guardar](../dlgbox/open-and-save-as-dialog-boxes.md) .

Cuando el usuario selecciona una carpeta, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) devuelve el PIDL completo de la carpeta y su nombre para mostrar. Si la carpeta está en el sistema de archivos, la aplicación puede convertir PIDL en una ruta de acceso llamando a [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista). La aplicación también puede restringir el intervalo de carpetas del que el usuario puede seleccionar especificando una carpeta raíz. Solo se mostrarán las carpetas que están por debajo de esa raíz en el espacio de nombres. En la ilustración siguiente se muestra el cuadro de diálogo **SHBrowseForFolder** , con la carpeta raíz establecida en archivos de programa.

![captura de pantalla del cuadro de diálogo Buscar carpeta](images/shell1.png)

Más adelante se proporciona un ejemplo sencillo de cómo usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) .

## <a name="special-folders-and-csidls"></a>Carpetas especiales y CSIDLs

Un número de carpetas usadas habitualmente se designa como *especial* en el sistema. Estas carpetas tienen un propósito bien definido y la mayoría están presentes en todos los sistemas. Incluso si no están presentes inicialmente, sus nombres y ubicaciones todavía están definidos, por lo que se pueden agregar posteriormente. La colección de carpetas especiales incluye todas las carpetas virtuales estándar del sistema, como las impresoras, mis documentos y el entorno de red. También incluye una serie de carpetas del sistema de archivos estándar, como archivos de programa y sistema.

Aunque las carpetas son un componente estándar de todos los sistemas, sus nombres y ubicaciones en el espacio de nombres pueden variar. Por ejemplo, el directorio del sistema es C: \\ WinNT \\ system32 en algunos sistemas y C: \\ Windows \\ system32 en otros. En el pasado, las variables de entorno proporcionaban una manera de determinar el nombre y la ubicación de una carpeta especial en un sistema determinado. El Shell ofrece ahora una forma más sólida y flexible de identificar carpetas especiales, [**CSIDLs**](csidl.md). En general, debe utilizarlos en lugar de variables de entorno.

CSIDLs proporcionan una forma uniforme de identificar y ubicar carpetas especiales, con independencia de su nombre o ubicación en un sistema determinado. A diferencia de las variables de entorno, CSIDLs se puede usar con carpetas virtuales, así como con carpetas del sistema de archivos. Cada carpeta especial tiene asignada una CSIDL única. Por ejemplo, la carpeta archivos de programa del sistema de archivos tiene **los \_ \_ archivos de programa** CSIDL de CSIDL y la carpeta virtual de entorno de red tiene la **\_ red** CSIDL de CSIDL.

Se usa CSIDL junto con una de varias funciones de Shell para recuperar el PIDL de una carpeta especial o una ruta de acceso de la carpeta del sistema de archivos especial. Si la carpeta no existe en un sistema, la aplicación puede obligar a que se cree mediante la combinación de su CSIDL con la **marca de CSIDL \_ \_ Create**. CSIDL se puede pasar a las siguientes funciones:

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), que recupera el PIDL de una carpeta especial.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), que recupera la ruta de acceso de una carpeta especial del sistema de archivos.

Tenga en cuenta que estas dos funciones se introdujeron con la versión 5,0 del shell y reemplazan las funciones [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) y [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Un ejemplo sencillo de cómo usar CSIDLs y SHBrowseForFolder

La siguiente función de ejemplo, PidlBrowse, muestra cómo usar CSIDLs para recuperar PIDL de una carpeta y usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) para que el usuario seleccione una carpeta. Devuelve el PIDL y el nombre para mostrar de la carpeta seleccionada.


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



La aplicación que realiza la llamada pasa un identificador de ventana, que es necesario para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). El parámetro *nCSIDL* es un CSIDL opcional que se usa para especificar una carpeta raíz. Solo se mostrarán las carpetas situadas debajo de la carpeta raíz en la jerarquía. La ilustración mostrada anteriormente se generó mediante una llamada a esta función con *nCSIDL* establecido en **\_ \_ los archivos de programa CSIDL**. La aplicación que realiza la llamada también pasa un búfer de cadena, *pszDisplayName*, para contener el nombre para mostrar de la carpeta seleccionada cuando PidlBrowse devuelve. Es responsabilidad de la aplicación que realiza la llamada liberar el IDList devuelto por **SHBrowseForFolder** mediante [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

 

 
