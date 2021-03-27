---
description: El Shell proporciona varias formas de administrar sistemas de archivos.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Administrar el sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b456ce1f26c128e6c3fc3bc9971672378a0d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360085"
---
# <a name="managing-the-file-system"></a>Administrar el sistema de archivos

El Shell proporciona varias formas de administrar sistemas de archivos. El Shell proporciona una función, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), que permite a una aplicación migrar, copiar, cambiar el nombre y eliminar archivos mediante programación. El shell también admite algunas capacidades adicionales de administración de archivos.

-   Los documentos HTML se pueden *conectar* a archivos relacionados, como archivos de gráficos o hojas de estilos. Cuando se mueve o se copia el documento, también se mueven o copian automáticamente los archivos conectados.
-   En el caso de los sistemas que están disponibles para más de un usuario, los archivos se pueden administrar por usuario. Los usuarios tienen acceso sencillo a sus archivos de datos, pero no a los archivos que pertenecen a otros usuarios.
-   Si se agregan o modifican archivos de documento, se pueden agregar a la lista de documentos recientes del shell. Cuando el usuario hace clic en el comando **documentos** en el menú Inicio, aparece una lista de vínculos a los documentos.

En este documento se explica cómo funcionan estas tecnologías de administración de archivos. A continuación, se describe cómo usar el shell para desplazar, copiar, cambiar el nombre y eliminar archivos, y cómo administrar objetos en la papelera de reciclaje.

-   [Administración de archivos por usuario](#per-user-file-management)
-   [Carpetas Mis documentos y mis imágenes](#my-documents-and-my-pictures-folders)
-   [Archivos conectados](#connected-files)
-   [Mover, copiar, cambiar el nombre y eliminar archivos](#moving-copying-renaming-and-deleting-files)
    -   [Notificar al shell](#notifying-the-shell)
-   [Ejemplo sencillo de administración de archivos con SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Agregar archivos a la lista de documentos recientes del shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Administración de archivos Per-User

El shell de Windows 2000 permite asociar archivos a un usuario determinado para que los archivos permanezcan ocultos de otros usuarios. En lo que respecta al sistema de archivos, los archivos se almacenan en la carpeta de perfil del usuario; normalmente, C: \\ Documents and Settings \\ *Username* \\ en Windows 2000 Systems. Esta característica permite a muchos usuarios usar el mismo equipo, a la vez que mantiene la privacidad de sus archivos de otros usuarios. Distintos usuarios pueden tener distintos programas disponibles. También proporciona una manera sencilla para que los administradores y las aplicaciones almacenen cosas como archivos de inicialización (. ini) o de vínculo (. lnk). Por tanto, las aplicaciones pueden conservar un estado diferente para cada usuario y recuperar fácilmente ese estado concreto cuando sea necesario. También hay una carpeta de perfil para almacenar información que es común a todos los usuarios.

Dado que no es conveniente determinar qué usuario ha iniciado sesión y dónde se encuentran los archivos, las carpetas por usuario estándar son carpetas especiales y se identifican mediante [**CSIDL**](csidl.md). Por ejemplo, el archivo CSIDL para la carpeta de archivos de programa por usuario es CSIDL \_ programas. Si la aplicación llama a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno de los CSIDLs por usuario, la función devuelve el puntero a una lista de identificadores de elemento (PIDL) o a la ruta de acceso adecuada para el usuario que ha iniciado sesión actualmente. Si la aplicación necesita recuperar la ruta de acceso o el PIDL de la carpeta de perfil, la de CSIDL es el **\_ Perfil de CSIDL**.

## <a name="my-documents-and-my-pictures-folders"></a>Carpetas Mis documentos y mis imágenes

Uno de los iconos estándar que se encuentra en el escritorio es **Mis documentos**. Al abrir esta carpeta, contiene los archivos de documento del usuario actual. La instancia de escritorio de mis documentos es una carpeta virtual, que es un alias de la ubicación del sistema de archivos que se usa para almacenar físicamente los documentos del usuario, que se encuentra inmediatamente debajo del escritorio en la jerarquía de espacios de nombres.

El propósito de las carpetas Mis documentos y mis imágenes es proporcionar una forma sencilla y segura de que los usuarios tengan acceso a sus archivos de documento e imagen en un sistema que pueda tener varios usuarios. A cada usuario se le asignan carpetas de sistema de archivos independientes para sus archivos. Por ejemplo, la ubicación de la carpeta de documentos de un usuario en el sistema de archivos suele ser algo como C: \\ Documents and Settings \\ *username* \\ My Documents. No es necesario que los usuarios sepan nada sobre la ubicación física de las carpetas del sistema de archivos. Simplemente tienen acceso a sus archivos a través del icono mis documentos.

> [!Note]  
> Mis documentos permite a un usuario tener acceso a sus propios archivos, pero no a los de otros usuarios. Si varias personas usan el mismo equipo, un administrador puede bloquear a los usuarios de la parte del sistema de archivos donde se almacenan los archivos reales. Así, los usuarios podrán trabajar en sus propios documentos a través de la carpeta Mis documentos, pero no de los documentos que pertenezcan a otros usuarios.

 

Normalmente, no es necesario que una aplicación sepa qué usuario ha iniciado sesión o dónde se encuentra en el sistema de archivos de la carpeta Mis documentos del usuario. En su lugar, la aplicación puede recuperar el PIDL del icono de escritorio mis documentos llamando al método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) del escritorio. El nombre de análisis usado para identificar la carpeta Mis documentos no es una ruta de acceso de archivo, sino:: {450d8fba-ad25-11d0-98a8-0800361b1103}. La expresión entre corchetes es la forma de texto del GUID mis documentos. Por ejemplo, para recuperar el PIDL de mis documentos, la aplicación debe usar esta llamada a **IShellFolder::P arsedisplayname**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Una vez que la aplicación tiene el PIDL mis documentos, puede controlar la carpeta tal como lo haría con una carpeta del sistema de archivos normal: enumerando elementos, analizando, enlazando y realizando cualquier otra operación de carpeta válida. El shell asigna automáticamente los cambios en mis documentos o en sus subcarpetas a las carpetas del sistema de archivos correspondientes.

Si la aplicación necesita tener acceso a la carpeta del sistema de archivos real que contiene los documentos del usuario actual, pase CSIDL \_ personal a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). La función devuelve el PIDL de la carpeta del sistema de archivos que se muestra en la carpeta Mis documentos del usuario actual.

## <a name="connected-files"></a>Archivos conectados

Los documentos HTML suelen tener un número de archivos de gráficos asociados, un archivo de hoja de estilos, varios archivos de Microsoft JScript (compatibles con la especificación del lenguaje ECMA 262), etc. Cuando se mueve o se copia el documento HTML principal, normalmente también se quieren trasladar o copiar los archivos asociados para evitar la interrupción de los vínculos. Desafortunadamente, no ha habido una manera fácil hasta ahora de determinar qué archivos están relacionados con cualquier documento HTML determinado que no sea mediante el análisis de su contenido. Para mitigar este problema, Windows 2000 proporciona una manera sencilla de *conectar* un documento HTML primario a su grupo de archivos asociados. Si está habilitada la conexión de archivos, cuando se mueva o copie el documento, todos los archivos conectados Irán con él.

Para crear un grupo de archivos conectados, el documento principal debe tener una extensión de nombre de archivo. htm o. html. Cree una subcarpeta de la carpeta principal del documento primario. El nombre de la subcarpeta debe ser el nombre del documento principal, menos la extensión. htm o. html, seguido de una de las extensiones que se enumeran a continuación. Las extensiones que se usan con más frecuencia son ". files" o " \_ files". Por ejemplo, si el documento principal se denomina MyDoc.htm, el nombre de la subcarpeta " \_ archivos MyDoc" define la subcarpeta como el contenedor de los archivos conectados del documento. Si se mueve o se copia el documento principal, también se mueven o copian las subcarpetas y sus archivos.

En algunos idiomas, es posible usar un equivalente localizado de " \_ archivos" para crear una subcarpeta para los archivos conectados. En la tabla siguiente se enumeran las cadenas válidas que se pueden anexar a un nombre de documento para crear una subcarpeta de archivos conectados. Tenga en cuenta que algunas de estas cadenas tienen '-' como primer carácter en lugar de ' \_ ' o '. '.



|              |               |                 |               |
|--------------|---------------|-----------------|---------------|
| " \_ archivaos" | " \_ arquivos"  | " \_ comstando"   | " \_ Bylos"     |
| "-Dateien"   | " \_ datoteke"  | " \_ dosyalar"    | " \_ elemei"    |
| " \_ failid"   | " \_ error"     | " \_ fajlovi"     | " \_ ficheiros" |
| " \_ fichiers" | "-File"      | ". files"        | " \_ archivos"     |
| " \_ archivo"     | " \_ fitxers"   | " \_ fitxategiak" | " \_ pliki"     |
| " \_ soubory"  | " \_ tiedostot" |                 |               |



 

> [!Note]  
> Esta característica es sensible a las mayúsculas y minúsculas de la extensión. Por ejemplo, para el ejemplo anterior, una subcarpeta denominada "MyDoc \_ files" no se conectará a MyDoc.htm.

 

El hecho de que la conexión de archivos esté habilitada o deshabilitada se controla mediante un valor de **reg \_ DWORD** , NoFileFolderConnection, de la siguiente clave del registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Normalmente, este valor no está definido y la conexión de archivos está habilitada. Si es necesario, puede deshabilitar la conexión de archivos agregando este valor a la clave y estableciéndolo en 1. Para habilitar la conexión de archivos de nuevo, establezca NoFileFolderConnection en cero.

> [!Note]  
> Normalmente, la conexión de archivos debe estar habilitada porque otras aplicaciones podrían depender de ella. Deshabilite la conexión de archivos solo si es absolutamente necesario.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Mover, copiar, cambiar el nombre y eliminar archivos

El espacio de nombres no es estático y las aplicaciones normalmente necesitan administrar el sistema de archivos mediante una de las siguientes operaciones.

-   Copiar un objeto en otra carpeta.
-   Mover un objeto a otra carpeta.
-   Eliminar un objeto.
-   Cambiar el nombre de un objeto.

Todas estas operaciones se realizan con [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Esta función toma uno o más archivos de código fuente y genera los archivos de destino correspondientes. En el caso de la operación de eliminación, el sistema intenta colocar los archivos eliminados en la papelera de reciclaje.

También es posible migrar archivos mediante la funcionalidad de [arrastrar y colocar](dragdrop.md) .

Para usar la función, debe rellenar los miembros de una estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) y pasarlo a [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Los miembros clave de la estructura son **pFrom** y **pTo**.

El miembro **pFrom** es una cadena terminada en **null** que contiene uno o más nombres de archivo de código fuente. Estos nombres pueden ser rutas de acceso completas o caracteres comodín de DOS estándar, como \* . \* Aunque este miembro se declara como una cadena terminada en **null**, se utiliza como búfer para contener varios nombres de archivo. El nombre de cada archivo debe terminar con el carácter **nulo** único habitual. Se debe anexar un carácter **nulo** adicional al final del nombre final para indicar el final de **pFrom**.

El miembro **pTo** es una cadena terminada en **null**, muy similar a **pFrom**. El miembro **pTo** contiene los nombres de uno o más nombres de destino completos. Se empaquetan en **pTo** de la misma manera que para **pFrom**. Si **pTo** contiene varios nombres, también debe establecer la marca **FoF \_ MULTIDESTFILES** en el miembro **fFlags** . El uso de **pTo** depende de la operación tal y como se describe aquí.

-   En el caso de las operaciones de copia y movimiento, si todos los archivos van a un solo directorio, **pTo** contiene el nombre de directorio completo. Si los archivos van a diferentes destinos, **pTo** también puede contener un nombre de archivo o directorio completo para cada archivo de código fuente. Si no existe un directorio, el sistema lo crea.
-   En el caso de las operaciones de cambio de nombre, **pTo** contiene una ruta de acceso completa para cada archivo de código fuente en **pFrom**.
-   Para las operaciones de eliminación, no se usa **pTo** .

### <a name="notifying-the-shell"></a>Notificar al shell

Notifique al shell el cambio después de usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para migrar, copiar, cambiar el nombre o eliminar archivos o después de realizar cualquier otra acción que afecte al espacio de nombres. Entre las acciones que deben ir acompañadas de la notificación se incluyen las siguientes:

-   Agregar o eliminar archivos o carpetas.
-   Mover, copiar o cambiar el nombre de archivos o carpetas.
-   Cambiar una asociación de archivo.
-   Cambiar atributos de archivo.
-   Adición o eliminación de unidades o medios de almacenamiento.
-   Crear o deshabilitar una carpeta compartida.
-   Cambiar la lista de imágenes del sistema.

Una aplicación notifica al shell llamando a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con los detalles de lo que ha cambiado. Después, el shell puede actualizar su imagen del espacio de nombres para reflejar con precisión su nuevo estado.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Ejemplo sencillo de administración de archivos con SHFileOperation

La siguiente aplicación de consola de ejemplo muestra el uso de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para copiar archivos de un directorio a otro. Los directorios de origen y de destino, C: \\ mis \_ documentos y c: \\ mis \_ Docs2, están codificados de forma rígida en la aplicación para que resulte más sencillo.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



La aplicación recupera primero un puntero a la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del escritorio. A continuación, recupera el PIDL del directorio de origen pasando su ruta de acceso completa a [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Tenga en cuenta que **IShellFolder::P arsedisplayname** requiere que la ruta de acceso del directorio sea una cadena Unicode. A continuación, la aplicación se enlaza al directorio de origen y utiliza su interfaz **IShellFolder** para recuperar la interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de un objeto de enumerador.

A medida que se enumeran todos los archivos del directorio de origen, se usa [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar su nombre. \_Se establece la marca SHGDN FORPARSING, que hace que **IShellFolder:: GetDisplayNameOf** devuelva la ruta de acceso completa del archivo. Las rutas de acceso de archivo, incluidos los caracteres **nulos** de terminación, se concatenan en una sola matriz, *szSourceFiles*. Se anexa un segundo carácter **nulo** a la ruta de acceso final para finalizar la matriz correctamente.

Una vez completada la enumeración, la aplicación asigna valores a una estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Tenga en cuenta que la matriz asignada a **pTo** para especificar el destino también debe terminar con un **valor null** doble. En este caso, simplemente se incluye en la cadena asignada a **pTo**. Dado que se trata de una aplicación de consola, las \_ marcas FoF Silent, FoF \_ noconfirm y FoF \_ NOCONFIRMMKDIR están configuradas para suprimir los cuadros de diálogo que puedan aparecer. Después de que [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) devuelve, se llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar el cambio al shell. A continuación, la aplicación realiza las operaciones de limpieza y devoluciones habituales.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Agregar archivos a la lista de documentos recientes del shell

El shell mantiene una lista de documentos agregados o modificados recientemente para cada usuario. El usuario puede mostrar una lista de vínculos a estos archivos haciendo clic en documentos en el menú Inicio. Al igual que con mis documentos, cada usuario tiene un directorio del sistema de archivos para contener los vínculos reales. Para recuperar el PIDL del directorio reciente del usuario actual, la aplicación puede llamar a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL \_ reciente, o bien llamar a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para recuperar su ruta de acceso.

La aplicación puede enumerar el contenido de la carpeta reciente mediante las técnicas descritas anteriormente en este documento. Sin embargo, una aplicación no debe modificar el contenido de la carpeta como si fuera una carpeta normal del sistema de archivos. Si lo hace, la lista de documentos recientes del shell no se actualizará correctamente y los cambios no se reflejarán en el menú Inicio. En su lugar, para agregar un vínculo de documento a la carpeta reciente de un usuario, la aplicación puede llamar a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). El shell agregará un vínculo a la carpeta del sistema de archivos correspondiente, así como la actualización de la lista de documentos recientes y el menú Inicio. También puede usar esta función para borrar la carpeta.

 

 
