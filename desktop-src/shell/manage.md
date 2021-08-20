---
description: Shell proporciona varias maneras de administrar sistemas de archivos.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Administración del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64bce2bea08794451d80fc4b1921baa21ee0fc26544b62ed9412d13b9bcb242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049234"
---
# <a name="managing-the-file-system"></a>Administración del sistema de archivos

Shell proporciona varias maneras de administrar sistemas de archivos. Shell proporciona una función, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), que permite a una aplicación mover, copiar, cambiar el nombre y eliminar archivos mediante programación. Shell también admite algunas funcionalidades de administración de archivos adicionales.

-   Los documentos HTML se *pueden conectar* a archivos relacionados, como archivos de gráficos o hojas de estilos. Cuando se mueve o copia el documento, los archivos conectados también se mueven o copian automáticamente.
-   En el caso de los sistemas que están disponibles para más de un usuario, los archivos se pueden administrar por usuario. Los usuarios tienen un acceso sencillo a sus archivos de datos, pero no a los archivos que pertenecen a otros usuarios.
-   Si se agregan o modifican archivos de documento, se pueden agregar a la lista de documentos recientes del shell. Cuando el usuario hace clic en el **comando Documentos** en la menú Inicio, aparece una lista de vínculos a los documentos.

En este documento se describe cómo funcionan estas tecnologías de administración de archivos. A continuación, se describe cómo usar el Shell para mover, copiar, cambiar el nombre y eliminar archivos, y cómo administrar objetos en el papelera de reciclaje.

-   [Administración de archivos por usuario](#per-user-file-management)
-   [carpetas Mis documentos y Mis imágenes](#my-documents-and-my-pictures-folders)
-   [Archivos conectados](#connected-files)
-   [Mover, copiar, cambiar el nombre y eliminar archivos](#moving-copying-renaming-and-deleting-files)
    -   [Notificación al shell](#notifying-the-shell)
-   [Ejemplo sencillo de administración de archivos con SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Agregar archivos a la lista de documentos recientes del shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Per-User file management

El Windows Shell 2000 permite que los archivos se asocie a un usuario determinado para que los archivos permanezcan ocultos para otros usuarios. En cuanto al sistema de archivos, los archivos se almacenan en la carpeta de perfil del usuario, normalmente C: Documentos y nombre de usuario Configuración en \\ \\  \\ Windows 2000 sistemas. Esta característica permite a muchas personas usar el mismo equipo, manteniendo al mismo tiempo la privacidad de sus archivos de otros usuarios. Los distintos usuarios pueden tener diferentes programas disponibles. También proporciona una manera sencilla para que los administradores y las aplicaciones almacenen cosas como la inicialización (.ini) o vincular archivos (.lnk). Por lo tanto, las aplicaciones pueden conservar un estado diferente para cada usuario y recuperar fácilmente ese estado concreto cuando sea necesario. También hay una carpeta de perfil para almacenar información que es común a todos los usuarios.

Dado que no es conveniente determinar qué usuario ha iniciado sesión y dónde se encuentran sus archivos, las carpetas estándar por usuario son carpetas especiales y se identifican mediante [**un CSIDL**](csidl.md). Por ejemplo, el CSIDL de la carpeta Archivos de programa por usuario es CSIDL \_ PROGRAMS. Si la aplicación llama a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno de los CSIDL por usuario, la función devuelve el puntero a una lista de identificadores de elemento (PIDL) o una ruta de acceso adecuada para el usuario que ha iniciado sesión actualmente. Si la aplicación necesita recuperar la ruta de acceso o PIDL de la carpeta del perfil, su CSIDL es **CSIDL \_ PROFILE**.

## <a name="my-documents-and-my-pictures-folders"></a>carpetas Mis documentos y Mis imágenes

Uno de los iconos estándar que se encuentran en el **escritorio es Mis documentos**. Al abrir esta carpeta, contiene los archivos de documento del usuario actual. La instancia de escritorio de Mis documentos es una carpeta virtual (un alias de la ubicación del sistema de archivos que se usa para almacenar físicamente los documentos del usuario) que se encuentra inmediatamente debajo del escritorio en la jerarquía de espacios de nombres.

El propósito de las carpetas Mis documentos y Mis imágenes es proporcionar una manera sencilla y segura para que los usuarios accedan a sus archivos de documento e imagen en un sistema que podría tener varios usuarios. A cada usuario se le asignan carpetas del sistema de archivos independientes para sus archivos. Por ejemplo, la ubicación de la carpeta de documentos de un usuario en el sistema de archivos suele ser algo parecido a C: Documentos y Configuración nombre de \\ \\  \\ usuario Mis documentos. No es necesario que los usuarios sepan nada sobre la ubicación física de sus carpetas del sistema de archivos. Simplemente acceden a sus archivos a través Mis documentos icono.

> [!Note]  
> Mis documentos permite que un usuario acceda a sus propios archivos, pero no a los de ningún otro usuario. Si varias personas usan el mismo equipo, un administrador puede bloquear a los usuarios de la parte del sistema de archivos donde se almacenan los archivos reales. Por lo tanto, los usuarios podrán trabajar en sus propios documentos a través de la carpeta Mis documentos, pero no en documentos que pertenezcan a otros usuarios.

 

Normalmente no es necesario que una aplicación sepa qué usuario ha iniciado sesión o dónde se encuentra en el sistema de archivos la carpeta de Mis documentos del usuario. En su lugar, la aplicación puede recuperar el PIDL del icono de escritorio Mis documentos mediante una llamada al método [**IShellFolder::P arseDisplayName del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) escritorio. El nombre de análisis usado para identificar la carpeta Mis documentos no es una ruta de acceso de archivo, sino ::{450d8fba-ad25-11d0-98a8-0800361b1103}. La expresión entre corchetes es la forma de texto Mis documentos GUID. Por ejemplo, para recuperar el PIDL de Mis documentos, la aplicación debe usar esta llamada a **IShellFolder::P arseDisplayName**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Una vez que la aplicación tiene Mis documentos PIDL, puede controlar la carpeta igual que lo haría con una carpeta normal del sistema de archivos: enumerar elementos, analizar, enlazar y realizar cualquier otra operación de carpeta válida. El Shell asigna automáticamente los cambios de Mis documentos sus subcarpetas a las carpetas del sistema de archivos adecuadas.

Si la aplicación necesita acceso a la carpeta del sistema de archivos real que contiene los documentos del usuario actual, pase CSIDL PERSONAL a \_ [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). La función devuelve el PIDL de la carpeta del sistema de archivos que se muestra en la carpeta de Mis documentos del usuario actual.

## <a name="connected-files"></a>Archivos conectados

Los documentos HTML suelen tener varios archivos de gráficos asociados, un archivo de hoja de estilos, varios archivos de Microsoft JScript (compatibles con la especificación del lenguaje ECMA 262), y así sucesivamente. Al mover o copiar el documento HTML principal, normalmente también desea mover o copiar sus archivos asociados para evitar vínculos importantes. Desafortunadamente, hasta ahora no ha habido ninguna manera fácil de determinar qué archivos están relacionados con un documento HTML determinado que no sea mediante el análisis de su contenido. Para mitigar este problema, Windows 2000 proporciona una manera sencilla de conectar un documento HTML principal *a* su grupo de archivos asociados. Si la conexión de archivos está habilitada, cuando se mueve o copia el documento, todos sus archivos conectados van con él.

Para crear un grupo de archivos conectados, el documento principal debe tener una .htm o .html extensión de nombre de archivo. Cree una subcarpeta de la carpeta primaria del documento principal. El nombre de la subcarpeta debe ser el nombre del documento principal, menos la extensión .htm o .html, seguida de una de las extensiones que se enumeran a continuación. Las extensiones más usadas son ".files" o \_ "files". Por ejemplo, si el documento principal se denomina MyDoc.htm, al asignar un nombre a la subcarpeta "MyDoc files" se define la subcarpeta como contenedor de los archivos conectados \_ del documento. Si se mueve o copia el documento principal, la subcarpeta y sus archivos también se mueven o copian.

Para algunos lenguajes, es posible usar un equivalente localizado de \_ "archivos" para crear una subcarpeta para los archivos conectados. En la tabla siguiente se enumeran las cadenas válidas que se pueden anexar a un nombre de documento para crear una subcarpeta de archivos conectados. Tenga en cuenta que algunas de estas cadenas tienen "-" como primer carácter en lugar de \_ "" o ".".



:::row:::
   :::column span="":::
      " \_ archivos"
   :::column-end:::
   :::column span="":::
      \_"arquivos"
   :::column-end:::
   :::column span="":::
      \_"bestanden"
   :::column-end:::
   :::column span="":::
      " \_ bylos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-Dateien"
   :::column-end:::
   :::column span="":::
      \_"datoteke"
   :::column-end:::
   :::column span="":::
      \_"dosyalar"
   :::column-end:::
   :::column span="":::
      \_"elemei"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ failid"
   :::column-end:::
   :::column span="":::
      " \_ produce un error"
   :::column-end:::
   :::column span="":::
      " \_ fa faq"
   :::column-end:::
   :::column span="":::
      \_"fichdores"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"fichiers"
   :::column-end:::
   :::column span="":::
      "-filer"
   :::column-end:::
   :::column span="":::
      ".files"
   :::column-end:::
   :::column span="":::
      " \_ files"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ file"
   :::column-end:::
   :::column span="":::
      \_"fitxers"
   :::column-end:::
   :::column span="":::
      \_"fitxategiak"
   :::column-end:::
   :::column span="":::
      " \_ pliki"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      \_"soubory"
   :::column-end:::
   :::column span="":::
      \_"tiedostot"
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> Esta característica es sensible al caso de la extensión. Por ejemplo, para el ejemplo anterior, una subcarpeta denominada "MyDoc Files" no se conectará a \_ MyDoc.htm.

 

Si la conexión de archivos está habilitada o deshabilitada se controla mediante un **valor REG \_ DWORD,** NoFileFolderConnection, de la siguiente clave del Registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Normalmente, este valor no está definido y la conexión de archivos está habilitada. Si es necesario, puede deshabilitar la conexión de archivos agregando este valor a la clave y estableciéndole en 1. Para volver a habilitar la conexión de archivos, establezca NoFileFolderConnection en cero.

> [!Note]  
> Normalmente, la conexión de archivos debe habilitarse porque otras aplicaciones pueden depender de ella. Deshabilite la conexión de archivos solo si es absolutamente necesario.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Mover, copiar, cambiar el nombre y eliminar archivos

El espacio de nombres no es estático y las aplicaciones normalmente necesitan administrar el sistema de archivos mediante una de las siguientes operaciones.

-   Copiar un objeto en otra carpeta.
-   Mover un objeto a otra carpeta.
-   Eliminar un objeto.
-   Cambiar el nombre de un objeto.

Todas estas operaciones se realizan con [**SHFileOperation.**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) Esta función toma uno o varios archivos de origen y genera los archivos de destino correspondientes. En el caso de la operación de eliminación, el sistema intenta colocar los archivos eliminados en el papelera de reciclaje.

También es posible mover archivos mediante la [funcionalidad de arrastrar y](dragdrop.md) colocar.

Para usar la función , debe rellenar los miembros de una estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) y pasarla a [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Los miembros clave de la estructura son **pFrom** y **pTo**.

El **miembro pFrom** es una cadena **terminada** en null doble que contiene uno o varios nombres de archivo de origen. Estos nombres pueden ser rutas de acceso completas o caracteres comodín dos estándar, como \* \* . Aunque este miembro se declara como una cadena terminada en **NULL,** se usa como búfer para contener varios nombres de archivo. El carácter NULL único habitual debe terminar cada nombre **de** archivo. Se debe **anexar** un carácter NULL adicional al final del nombre final para indicar el final de **pFrom**.

El **miembro pTo** es una cadena **terminada** en null doble, muy parecido a **pFrom**. El **miembro pTo** contiene los nombres de uno o varios nombres de destino completos. Se empaquetan en **pTo de la** misma manera que para **pFrom**. Si **pTo** contiene varios nombres, también debe establecer la marca **\_ FOF MULTIDESTFILES** en el **miembro fFlags.** El uso de **pTo** depende de la operación como se describe aquí.

-   Para las operaciones de copia y movimiento, si todos los archivos van a un único directorio, **pTo** contiene el nombre completo del directorio. Si los archivos van a destinos diferentes, **pTo** también puede contener un directorio completo o un nombre de archivo para cada archivo de origen. Si no existe un directorio, el sistema lo crea.
-   Para las operaciones de cambio de nombre, **pTo** contiene una ruta de acceso completa para cada archivo de origen en **pFrom**.
-   Para las operaciones de eliminación, no se usa **pTo.**

### <a name="notifying-the-shell"></a>Notificación al shell

Notifique al Shell el cambio después de usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para mover, copiar, cambiar el nombre o eliminar archivos, o después de realizar cualquier otra acción que afecte al espacio de nombres. Entre las acciones que deben ir acompañadas de la notificación se incluyen las siguientes:

-   Agregar o eliminar archivos o carpetas.
-   Mover, copiar o cambiar el nombre de archivos o carpetas.
-   Cambio de una asociación de archivos.
-   Cambio de atributos de archivo.
-   Agregar o quitar unidades o medios de almacenamiento.
-   Crear o deshabilitar una carpeta compartida.
-   Cambiar la lista de imágenes del sistema.

Una aplicación notifica al Shell mediante una llamada a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con los detalles de lo que ha cambiado. A continuación, el Shell puede actualizar su imagen del espacio de nombres para reflejar con precisión su nuevo estado.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Ejemplo sencillo de administración de archivos con SHFileOperation

En la siguiente aplicación de consola de ejemplo se muestra el uso de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para copiar archivos de un directorio a otro. Los directorios de origen y destino, C: My Docs y \\ \_ C: \\ My Docs2, están codificados de forma fuerte en la aplicación para \_ simplificar.


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



En primer lugar, la aplicación recupera un puntero a la interfaz [**IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) escritorio. A continuación, recupera el PIDL del directorio de origen pasando su ruta de acceso completa a [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Tenga en **cuenta que IShellFolder::P arseDisplayName** requiere que la ruta de acceso del directorio sea una cadena Unicode. A continuación, la aplicación se enlaza al directorio de origen y usa su **interfaz IShellFolder** para recuperar la interfaz [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de un objeto enumerador.

A medida que se enumera cada archivo del directorio de origen, se usa [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar su nombre. Se establece la marca SHGDN FORPARSING, lo que hace que \_ **IShellFolder::GetDisplayNameOf** devuelva la ruta de acceso completa del archivo. Las rutas de acceso de archivo, incluidos los caracteres **NULL** de terminación, se concatenan en una sola matriz, *szSourceFiles*. Se anexa **un segundo** carácter NULL a la ruta de acceso final para finalizar correctamente la matriz.

Una vez completada la enumeración, la aplicación asigna valores a una [**estructura SHFILEOPSTRUCT.**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) Tenga en cuenta que la matriz asignada **a pTo** para especificar el destino también debe terminar con un valor **NULL doble.** En este caso, simplemente se incluye en la cadena que se asigna a **pTo**. Dado que se trata de una aplicación de consola, las marcas FOF \_ SILENT, FOF \_ NOCONFIRMATION y FOF NOCONFIRMMKDIR se establecen para suprimir los cuadros de diálogo que puedan \_ aparecer. Una [**vez que shfileoperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) devuelve, se llama a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar el cambio al shell. A continuación, la aplicación realiza la limpieza habitual y devuelve .

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Agregar archivos a la lista de documentos recientes del shell

El Shell mantiene una lista de documentos agregados o modificados recientemente para cada usuario. El usuario puede mostrar una lista de vínculos a estos archivos haciendo clic en Documentos en el menú Inicio. Al igual Mis documentos, cada usuario tiene un directorio del sistema de archivos para contener los vínculos reales. Para recuperar el PIDL del directorio Recent del usuario actual, la aplicación puede llamar a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL RECENT o llamar a \_ [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para recuperar su ruta de acceso.

La aplicación puede enumerar el contenido de la carpeta Recent mediante las técnicas que se han mencionado anteriormente en este documento. Sin embargo, una aplicación no debe modificar el contenido de la carpeta como si fuera una carpeta normal del sistema de archivos. Si lo hace, la lista de documentos recientes del Shell no se actualizará correctamente y los cambios no se reflejarán en el menú Inicio. En su lugar, para agregar un vínculo de documento a la carpeta Recent de un usuario, la aplicación puede llamar a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). El Shell agregará un vínculo a la carpeta del sistema de archivos adecuada, así como actualizará su lista de documentos recientes y el menú Inicio. También puede usar esta función para borrar la carpeta.

 

 
