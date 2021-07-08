---
description: Una vez que la aplicación ha ubicado un objeto de archivo, el paso siguiente suele ser actuar sobre él de alguna manera.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508616"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Una vez que la aplicación ha ubicado un objeto de archivo, el paso siguiente suele ser actuar sobre él de alguna manera. Por ejemplo, es posible que la aplicación quiera iniciar otra aplicación que permita al usuario modificar un archivo de datos. Si el archivo de interés es un archivo ejecutable, es posible que la aplicación simplemente quiera iniciarlo. En este documento se describe cómo usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para realizar estas tareas.

-   [Uso de ShellExecute y ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbos de objeto](#object-verbs)
    -   [Uso de ShellExecuteEx para proporcionar servicios de activación desde un sitio](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Usar ShellExecute para iniciar el cuadro de diálogo buscar](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Un ejemplo sencillo de cómo usar ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Uso de ShellExecute y ShellExecuteEx

Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)la aplicación debe especificar el objeto de archivo o carpeta en el que se va a actuar y un *verbo* que especifique la operación. Para **ShellExecute,** asigne estos valores a los parámetros adecuados. Para **ShellExecuteEx**, rellene los miembros adecuados de una [**estructura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) También hay otros miembros o parámetros que se pueden usar para ajustar el comportamiento de las dos funciones.

Los objetos de archivo y carpeta pueden formar parte del sistema de archivos u objetos virtuales, y se pueden identificar mediante rutas de acceso o punteros a listas de identificadores de elementos (PIDL).

### <a name="object-verbs"></a>Verbos de objeto

Los verbos disponibles para un objeto son básicamente los elementos que se encuentran en el menú contextual de un objeto. Para buscar qué verbos están disponibles, busque en el Registro en

**HKEY \_ CLASSES \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\ **Verbo de** \\ *shell*

donde *el \_ objeto clsid* es el identificador de clase (CLSID) del objeto y *verb* es el nombre del verbo disponible. La  \\ **subclave del** comando verbo contiene los datos que indican lo que sucede cuando se invoca ese verbo.

Para averiguar qué verbos están disponibles para los [objetos de Shell](handlers.md)predefinidos, busque en el Registro en

**HKEY \_ Verbo \_ de shell de** \\ *nombre de \_* \\ **objeto** \\  CLASSES ROOT

donde *el \_ nombre del* objeto es el nombre del objeto de Shell predefinido. De nuevo, *la* \\ **subclave del** comando verbo contiene los datos que indican lo que sucede cuando se invoca ese verbo.

Los verbos disponibles habitualmente incluyen:



| Verbo       | Descripción                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| edición       | Inicia un editor y abre el documento para su edición.                                                   |
| find       | Inicia una búsqueda a partir del directorio especificado.                                                |
| abierto       | Inicia una aplicación. Si este archivo no es un archivo ejecutable, se inicia su aplicación asociada. |
| imprimir      | Imprime el archivo de documento.                                                                                |
| properties | Muestra las propiedades del objeto.                                                                        |
| runas      | Inicia una aplicación como administrador. El Control de cuentas de usuario (UAC) solicitará al usuario su consentimiento para ejecutar la aplicación con privilegios elevados o escribirá las credenciales de una cuenta de administrador usada para ejecutar la aplicación. |



Cada verbo corresponde al comando que se usaría para iniciar la aplicación desde una ventana de consola. El **verbo** abierto es un buen ejemplo, ya que se admite normalmente. Para .exe archivos, **abrir** simplemente inicia la aplicación. Sin embargo, se usa con más frecuencia para iniciar una aplicación que funciona en un archivo determinado. Por ejemplo, Microsoft WordPad .txt abrir los archivos. El **verbo** abierto para un .txt archivo se correspondería con algo parecido al comando siguiente:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Cuando se [**usa ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir un archivo .txt, Wordpad.exe se inicia con el archivo especificado como argumento. Algunos comandos pueden tener argumentos adicionales, como marcas, que se pueden agregar según sea necesario para iniciar la aplicación correctamente. Para obtener más información sobre los menús contextuales y verbos, vea [Extender los menús contextuales.](context.md)

En general, intentar determinar la lista de verbos disponibles para un archivo determinado es un poco complicado. En muchos casos, simplemente puede establecer el parámetro *lpVerb* en **NULL,** que invoca el comando predeterminado para el tipo de archivo. Este procedimiento suele ser equivalente a establecer *lpVerb* en "open", pero algunos tipos de archivo pueden tener un comando predeterminado diferente. Para obtener más información, vea [Extender los menús contextuales y](context.md) la documentación de referencia de [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Uso de ShellExecuteEx para proporcionar servicios de activación desde un sitio

Los servicios de una cadena de sitios pueden controlar muchos comportamientos de activación de elementos. A Windows 8, puede proporcionar un puntero a la cadena de sitio a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar estos comportamientos. Para proporcionar el sitio a **ShellExecuteEx**:

-   Especifique la marca SEE MASK FLAG OF IS SITE en el \_ \_ miembro \_ \_ \_ **fMask** [**de SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Proporcione el [**IUnknown en**](/windows/win32/api/unknwn/nn-unknwn-iunknown) el **miembro hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Usar ShellExecute para iniciar el cuadro de diálogo buscar

Cuando un usuario hace clic con el botón derecho en un icono de carpeta en Windows Explorer, uno de los elementos de menú es "Buscar". Si seleccionan ese elemento, shell inicia su utilidad De búsqueda. Esta utilidad muestra un cuadro de diálogo que se puede usar para buscar en archivos una cadena de texto especificada. Una aplicación puede iniciar mediante programación la utilidad Search para un directorio llamando a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "find" como parámetro *lpVerb* y la ruta de acceso del directorio como parámetro *lpFile.* Por ejemplo, la siguiente línea de código inicia la utilidad Search para el directorio c: \\ MyPrograms.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Un ejemplo sencillo de cómo usar ShellExecuteEx

En la siguiente aplicación de consola de ejemplo se muestra el uso de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). La mayoría del código de comprobación de errores se ha omitido para mayor claridad.


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



En primer lugar, la aplicación recupera el PIDL del directorio Windows y enumera su contenido hasta que encuentra el primer .bmp archivo. A diferencia del ejemplo anterior, [**se usa IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar el nombre de análisis del archivo en lugar de su nombre para mostrar. Dado que se trata de una carpeta del sistema de archivos, el nombre del análisis es una ruta de acceso completa, que es lo que se necesita [**para ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

Una vez que se .bmp el primer archivo, se asignan los valores adecuados a los miembros de una [**estructura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) El **miembro lpFile** se establece en el nombre de análisis del archivo y el miembro **lpVerb** en **NULL** para comenzar la operación predeterminada. En este caso, la operación predeterminada es "open". A continuación, la estructura se pasa a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), que inicia el controlador predeterminado para los archivos de mapa de bits, normalmente MSPaint.exe, para abrir el archivo. Una vez que se devuelve la función, se liberan los PIDL y se libera Windows interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta.

 

 
