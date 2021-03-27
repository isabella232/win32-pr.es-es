---
description: Una vez que la aplicación ha encontrado un objeto de archivo, el paso siguiente suele actuar sobre él de alguna manera.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908745"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Una vez que la aplicación ha encontrado un objeto de archivo, el paso siguiente suele actuar sobre él de alguna manera. Por ejemplo, es posible que la aplicación desee iniciar otra aplicación que permita al usuario modificar un archivo de datos. Si el archivo de interés es un ejecutable, es posible que la aplicación desee simplemente iniciarlo. En este documento se explica cómo usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para realizar estas tareas.

-   [Usar ShellExecute y ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbos de objeto](#object-verbs)
    -   [Usar ShellExecuteEx para proporcionar servicios de activación desde un sitio](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Usar ShellExecute para iniciar el cuadro de diálogo de búsqueda](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Un ejemplo sencillo de cómo usar ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Usar ShellExecute y ShellExecuteEx

Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), la aplicación debe especificar el objeto de archivo o carpeta en el que se actuará y un *verbo* que especifique la operación. Para **ShellExecute**, asigne estos valores a los parámetros adecuados. En el caso de **ShellExecuteEx**, rellene los miembros adecuados de una estructura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . También hay otros miembros o parámetros que se pueden usar para ajustar el comportamiento de las dos funciones.

Los objetos de archivos y carpetas pueden formar parte del sistema de archivos o de los objetos virtuales, y se pueden identificar mediante rutas de acceso o punteros a listas de identificadores de elementos (PIDL).

### <a name="object-verbs"></a>Verbos de objeto

Los verbos disponibles para un objeto son esencialmente los elementos que se encuentran en el menú contextual de un objeto. Para averiguar qué verbos están disponibles, busque en el registro en

**HKEY \_ Clases \_** \\ **CLSID** raíz \\ *{Object \_ CLSID}* \\ **Shell** \\ *Verb*

donde el *objeto \_ CLSID* es el identificador de clase (CLSID) del objeto y *Verb* es el nombre del verbo disponible. La  \\ subclave del **comando** Verb contiene los datos que indican lo que ocurre cuando se invoca ese verbo.

Para averiguar qué verbos están disponibles para los [objetos de Shell predefinidos](handlers.md), busque en el registro en

**HKEY \_ \_** \\ *\_ Nombre de objeto* raíz de clases \\  \\ *verbo* de Shell

donde *Object \_ Name* es el nombre del objeto de Shell predefinido. Una vez más , la \\ subclave del **comando** Verb contiene los datos que indican lo que ocurre cuando se invoca ese verbo.

Los verbos disponibles comúnmente incluyen:



| Verbo       | Descripción                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| edición       | Inicia un editor y abre el documento para su edición.                                                   |
| find       | Inicia una búsqueda a partir del directorio especificado.                                                |
| abrir       | Inicia una aplicación. Si este archivo no es un archivo ejecutable, se inicia su aplicación asociada. |
| imprimir      | Imprime el archivo de documento.                                                                                |
| properties | Muestra las propiedades del objeto.                                                                        |
| runas      | Inicia una aplicación como administrador. Control de cuentas de usuario (UAC) solicitará al usuario su consentimiento para |
|            | Ejecute la aplicación con privilegios elevados o escriba las credenciales de una cuenta de administrador usada para ejecutar el        |
|            | aplicación Aha!.                                                                                             |

 

Cada verbo corresponde al comando que se utilizaría para iniciar la aplicación desde una ventana de consola. El verbo **Open** es un buen ejemplo, ya que normalmente se admite. En el caso de los archivos. exe, **abra** simplemente inicia la aplicación. Sin embargo, se suele usar para iniciar una aplicación que funciona en un archivo determinado. Por ejemplo, Microsoft WordPad puede abrir los archivos. txt. El verbo **Open** de un archivo. txt se correspondería a algo como el comando siguiente:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Al usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir un archivo. txt, Wordpad.exe se inicia con el archivo especificado como su argumento. Algunos comandos pueden tener argumentos adicionales, como marcas, que se pueden agregar según sea necesario para iniciar la aplicación correctamente. Para obtener más información sobre los menús contextuales y los verbos, vea [extender los menús contextuales](context.md).

En general, intentar determinar la lista de verbos disponibles para un archivo determinado es algo complicado. En muchos casos, puede simplemente establecer el parámetro *lpVerb* en **null**, que invoca el comando predeterminado para el tipo de archivo. Este procedimiento suele ser equivalente a establecer *lpVerb* en "Open", pero algunos tipos de archivo pueden tener un comando predeterminado diferente. Para obtener más información, consulte extensión de los [menús contextuales](context.md) y la documentación de referencia de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Usar ShellExecuteEx para proporcionar servicios de activación desde un sitio

Los servicios de una cadena de sitios pueden controlar muchos comportamientos de activación de elementos. A partir de Windows 8, puede proporcionar un puntero a la cadena de sitios a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar estos comportamientos. Para proporcionar el sitio a **ShellExecuteEx**:

-   Especifique la marca de \_ máscara See \_ \_ HINST \_ is \_ site Flag en el miembro **fMask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Proporcione [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el miembro **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Usar ShellExecute para iniciar el cuadro de diálogo de búsqueda

Cuando un usuario hace clic con el botón secundario en un icono de carpeta en el explorador de Windows, uno de los elementos de menú es "Buscar". Si seleccionan ese elemento, el shell inicia su utilidad de búsqueda. Esta utilidad muestra un cuadro de diálogo que se puede usar para buscar en archivos una cadena de texto especificada. Una aplicación puede iniciar mediante programación la utilidad de búsqueda para un directorio llamando a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "Find" como parámetro *lpVerb* y la ruta de acceso del directorio como el parámetro *lpFile* . Por ejemplo, la siguiente línea de código inicia la utilidad de búsqueda para el directorio c: mis \\ programas.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Un ejemplo sencillo de cómo usar ShellExecuteEx

La siguiente aplicación de consola de ejemplo muestra el uso de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). La mayoría del código de comprobación de errores se ha omitido para mayor claridad.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



En primer lugar, la aplicación recupera el PIDL del directorio de Windows y enumera su contenido hasta que encuentra el primer archivo. bmp. A diferencia del ejemplo anterior, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) se usa para recuperar el nombre de análisis del archivo en lugar de su nombre para mostrar. Dado que se trata de una carpeta del sistema de archivos, el nombre de análisis es una ruta de acceso completa, que es lo que se necesita para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

Una vez que se encuentra el primer archivo. bmp, los valores adecuados se asignan a los miembros de una estructura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . El miembro **lpFile** se establece en el nombre de análisis del archivo y el miembro **lpVerb** en **null** para comenzar la operación predeterminada. En este caso, la operación predeterminada es "Open". A continuación, la estructura se pasa a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), que inicia el controlador predeterminado para los archivos de mapa de bits, normalmente MSPaint.exe, para abrir el archivo. Una vez que la función devuelve, se liberan los PIDL y se libera la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta Windows.

 

 
