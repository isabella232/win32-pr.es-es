---
description: Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtención del identificador de una carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d75051d52f0dfcee54b6365a8f546d2cbda2c3b5f7c0f4b6fbbc19fa1e40c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459014"
---
# <a name="getting-a-folders-id"></a>Obtención del identificador de una carpeta

Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo. Esto significa obtener su puntero a una lista de identificadores de elemento (PIDL) o, en el caso de los objetos del sistema de archivos, su ruta de acceso. En esta sección se de analizan dos de las maneras más sencillas de obtener los IDs de objeto.

Para obtener un enfoque más eficaz que funcione con cualquier carpeta, use la [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Consulte [Obtención de información sobre el contenido de una carpeta para](folder-info.md) obtener más detalles.

-   [Cuadro de diálogo OpenFiles](#the-openfiles-dialog-box)
-   [Cuadro de diálogo SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Carpetas especiales y CSIDL](#special-folders-and-csidls)
-   [Un ejemplo sencillo de cómo usar los CSIDL y SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>Cuadro de diálogo OpenFiles

Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede usar la [**interfaz IFileDialog.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) Al llamar a esta interfaz **con la marca \_ PICKFOLDERS de FOS,** se inicia el cuadro de [diálogo](../dlgbox/open-and-save-as-dialog-boxes.md) Común abrir archivos en modo "seleccionar carpetas".

Para Windows Vista y versiones posteriores, esta es la manera recomendada de elegir carpetas.

## <a name="the-shbrowseforfolder-dialog-box"></a>Cuadro de diálogo SHBrowseForFolder

Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede invocar simplemente [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Al llamar a esta función, se inicia un cuadro de diálogo con una interfaz de usuario que funciona de forma similar a los cuadros de diálogo comunes Abrir [o](../dlgbox/open-and-save-as-dialog-boxes.md) Guardar como .

Cuando el usuario selecciona una carpeta, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) devuelve el PIDL completo de la carpeta y su nombre para mostrar. Si la carpeta está en el sistema de archivos, la aplicación puede convertir pidl en una ruta de acceso llamando a [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista). La aplicación también puede restringir el intervalo de carpetas que el usuario puede seleccionar especificando una carpeta raíz. Solo aparecerán las carpetas que están por debajo de esa raíz en el espacio de nombres . En la ilustración siguiente se muestra **el cuadro de diálogo SHBrowseForFolder,** con la carpeta raíz establecida en Archivos de programa.

![captura de pantalla del cuadro de diálogo Buscar carpeta](images/shell1.png)

Más adelante se proporciona un ejemplo sencillo [**de cómo usar SHBrowseForFolder.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)

## <a name="special-folders-and-csidls"></a>Carpetas especiales y CSIDL

El sistema designa una serie de carpetas que se usan con frecuencia *como* especiales. Estas carpetas tienen un propósito bien definido y la mayoría de ellas están presentes en todos los sistemas. Incluso si no están presentes inicialmente, sus nombres y ubicaciones todavía están definidos, por lo que se pueden agregar más adelante. La colección de carpetas especiales incluye todas las carpetas virtuales estándar del sistema, como Impresoras, Mis documentos y Network Neighborhood. También incluye varias carpetas estándar del sistema de archivos, como Archivos de programa y Sistema.

Aunque las carpetas son un componente estándar de todos los sistemas, sus nombres y ubicaciones en el espacio de nombres pueden variar. Por ejemplo, el directorio System es C: Winnt System32 en algunos sistemas y \\ \\ C: \\ Windows \\ System32 en otros. En el pasado, las variables de entorno proporcionaba una manera de determinar el nombre y la ubicación de una carpeta especial en un sistema determinado. Shell ahora proporciona una manera más sólida y flexible de identificar carpetas especiales, [**CSIDL.**](csidl.md) Por lo general, debe usarlos en lugar de variables de entorno.

Los CSIDL proporcionan una manera uniforme de identificar y buscar carpetas especiales, independientemente de su nombre o ubicación en un sistema determinado. A diferencia de las variables de entorno, los CSIDL se pueden usar con carpetas virtuales, así como con carpetas del sistema de archivos. Cada carpeta especial tiene asignado un CSIDL único. Por ejemplo, la carpeta del sistema de archivos archivos de programa tiene un CSIDL de ARCHIVOS DE PROGRAMA **CSIDL \_ \_** y la carpeta virtual Network Neighborhood tiene un CSIDL de **CSIDL \_ NETWORK.**

Un CSIDL se usa junto con una de varias funciones de Shell para recuperar el PIDL de una carpeta especial o la ruta de acceso de una carpeta especial del sistema de archivos. Si la carpeta no existe en un sistema, la aplicación puede forzar su creación combinando su CSIDL con **CSIDL \_ FLAG \_ CREATE**. El CSIDL se puede pasar a las funciones siguientes:

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), que recupera el PIDL de una carpeta especial.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), que recupera la ruta de acceso de una carpeta especial del sistema de archivos.

Tenga en cuenta que estas dos funciones se introdujeron con la versión 5.0 del shell y sustituyen a las funciones [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) y [**SHGetSpecialFolderPath.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha)

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Un ejemplo sencillo de cómo usar los CSIDL y SHBrowseForFolder

La siguiente función de ejemplo, PidlBrowse, muestra cómo usar los CSIDL para recuperar el PIDL de una carpeta y usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) para que el usuario seleccione una carpeta. Devuelve el PIDL y el nombre para mostrar de la carpeta seleccionada.


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



La aplicación que realiza la llamada pasa un identificador de ventana, que es necesario para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). El *parámetro nCSIDL* es un CSIDL opcional que se usa para especificar una carpeta raíz. Solo se mostrarán las carpetas debajo de la carpeta raíz de la jerarquía. La ilustración mostrada anteriormente se generó mediante una llamada a esta función con *nCSIDL* establecido en **CSIDL \_ PROGRAM \_ FILES**. La aplicación que realiza la llamada también pasa un búfer de cadena, *pszDisplayName*, para contener el nombre para mostrar de la carpeta seleccionada cuando pidlBrowse devuelve. Es responsabilidad de la aplicación que realiza la llamada liberar el IDList devuelto por **SHBrowseForFolder** mediante [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

 

 
