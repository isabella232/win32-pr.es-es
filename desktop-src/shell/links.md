---
description: Un vínculo de Shell es un objeto de datos que contiene información que se usa para tener acceso a otro objeto en el espacio de nombres del shell&\# 8212; es decir, cualquier objeto visible a través del explorador de Windows.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Vínculos de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277416"
---
# <a name="shell-links"></a>Vínculos de Shell

Un *vínculo de Shell* es un objeto de datos que contiene información que se usa para tener acceso a otro objeto en el espacio de nombres del shell, es decir, cualquier objeto visible a través del explorador de Windows. Los tipos de objetos a los que se puede tener acceso a través de vínculos de Shell incluyen archivos, carpetas, unidades de disco e impresoras. Un vínculo de Shell permite a un usuario o una aplicación tener acceso a un objeto desde cualquier lugar del espacio de nombres. El usuario o la aplicación no necesita conocer el nombre y la ubicación actuales del objeto.

-   [Acerca de los vínculos de Shell](#about-shell-links)
    -   [Resolución de vínculo](#link-resolution)
    -   [Archivos de vínculo](#link-files)
    -   [Identificadores de elementos y listas de identificadores](#item-identifiers-and-identifier-lists)
-   [Usar vínculos de Shell](#using-shell-links)
    -   [Crear un acceso directo y un acceso directo a una carpeta en un archivo](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Resolución de un acceso directo](#resolving-a-shortcut)
    -   [Crear un acceso directo a un objeto que no es de archivo](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Acerca de los vínculos de Shell

El usuario crea un vínculo de Shell eligiendo el comando **crear acceso directo** en el menú contextual de un objeto. El sistema crea automáticamente un icono para el vínculo de Shell mediante la combinación del icono del objeto con una flecha pequeña (conocida como el icono de superposición de vínculos definida por el sistema) que aparece en la esquina inferior izquierda del icono. Un vínculo de Shell que tiene un icono se denomina acceso directo; sin embargo, los términos vínculo y acceso directo de Shell a menudo se usan indistintamente. Normalmente, el usuario crea accesos directos para obtener acceso rápido a los objetos almacenados en subcarpetas o en carpetas compartidas en otros equipos. Por ejemplo, un usuario puede crear un acceso directo a un documento de Microsoft Word que se encuentra en una subcarpeta y colocar el icono de acceso directo en el escritorio. Después, el usuario puede abrir el documento haciendo doble clic en el icono de acceso directo. Si el documento se mueve o se cambia de nombre después de crear el acceso directo, el sistema intentará actualizar el acceso directo la próxima vez que el usuario lo seleccione.

Las aplicaciones también pueden crear y usar vínculos de Shell y accesos directos. Por ejemplo, una aplicación de procesamiento de texto podría crear un vínculo de Shell para implementar una lista de los documentos usados más recientemente. Una aplicación crea un vínculo de Shell mediante la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para crear un objeto de vínculo de Shell. La aplicación usa la interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) para almacenar el objeto en un archivo o una secuencia.

> [!Note]  
> No se puede usar [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para crear un vínculo a una dirección URL.

 

En esta información general se describe la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) y se explica cómo usarla para crear y resolver vínculos de Shell desde una aplicación basada en Microsoft Win32. Dado que el diseño de vínculos de Shell se basa en el modelo de objetos componentes (COM) de OLE, debería estar familiarizado con los conceptos básicos de la programación de COM y OLE antes de leer esta información general.

### <a name="link-resolution"></a>Resolución de vínculo

Si un usuario crea un acceso directo a un objeto y posteriormente se cambia el nombre o la ubicación del objeto, el sistema toma automáticamente los pasos necesarios para actualizar el acceso directo la próxima vez que el usuario lo seleccione. Sin embargo, si una aplicación crea un vínculo de Shell y lo almacena en una secuencia, el sistema no intenta resolver el vínculo automáticamente. La aplicación debe resolver el vínculo llamando al método [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .

Cuando se crea un vínculo de Shell, el sistema guarda información sobre el vínculo. Al resolver un vínculo, ya sea de forma automática o con una llamada a [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) , el sistema recupera primero la ruta de acceso asociada con el vínculo de Shell mediante un puntero a la lista de identificadores del vínculo de Shell. Para obtener más información sobre la lista de identificadores, vea [identificadores de elementos y listas de identificadores](#item-identifiers-and-identifier-lists). El sistema busca el objeto asociado en esa ruta de acceso y, si encuentra el objeto, resuelve el vínculo. Si el sistema no encuentra el objeto, llama a en el servicio de [seguimiento de vínculos distribuidos](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT), si está disponible, para buscar el objeto. Si el servicio DLT no está disponible o no encuentra el objeto, el sistema busca en el mismo directorio un objeto con la misma hora de creación de archivo y los mismos atributos, pero con un nombre diferente. Este tipo de búsqueda resuelve un vínculo a un objeto al que se ha cambiado el nombre.

Si el sistema sigue sin poder encontrar el objeto, busca en los directorios, en el escritorio y en los volúmenes locales, lo que busca de forma recursiva en el árbol de directorios de un objeto con el mismo nombre o la misma hora de creación. Si el sistema sigue sin encontrar una coincidencia, muestra un cuadro de diálogo que solicita al usuario una ubicación. Una aplicación puede suprimir el cuadro de diálogo especificando el valor de **\_ no la interfaz de \_ usuario de SLR** en una llamada a [**IShellLink:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Inicialización de la biblioteca de objetos de componentes

Para que una aplicación pueda crear y resolver accesos directos, debe inicializar la biblioteca de objetos componente llamando a la función [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Cada llamada a **CoInitialize** requiere una llamada correspondiente a la función [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , a la que una aplicación debe llamar cuando termina. La llamada a **CoUninitialize** garantiza que la aplicación no finaliza hasta que se han recibido todos los mensajes pendientes.

### <a name="location-independent-names"></a>Nombres de Location-Independent

El sistema proporciona nombres independientes de la ubicación para los vínculos de Shell a los objetos almacenados en carpetas compartidas. Si el objeto se almacena localmente, el sistema proporciona la ruta de acceso local y el nombre de archivo del objeto. Si el objeto se almacena de forma remota, el sistema proporciona un nombre de recurso de red UNC (Convención de nomenclatura universal) para el objeto. Dado que el sistema proporciona nombres independientes de la ubicación, un vínculo de Shell puede servir como nombre universal para un archivo que se puede transferir a otros equipos.

### <a name="link-files"></a>Archivos de vínculo

Cuando el usuario crea un acceso directo a un objeto eligiendo el comando **crear acceso directo** del menú contextual del objeto, Windows almacena la información que necesita para tener acceso al objeto en un archivo de vínculo, un archivo binario con la extensión de nombre de archivo. lnk. Un archivo de vínculo contiene la siguiente información:

-   La ubicación (ruta de acceso) del objeto al que hace referencia el acceso directo (llamado el objeto correspondiente).
-   Directorio de trabajo del objeto correspondiente.
-   Lista de argumentos que el sistema pasa al objeto correspondiente cuando se activa el método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para el acceso directo.
-   El comando show que se usa para establecer el estado de presentación inicial del objeto correspondiente. Éste es uno de los valores de SW \_ descritos en [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   La ubicación (ruta de acceso e índice) del icono del acceso directo.
-   Cadena de Descripción del acceso directo.
-   Método abreviado de teclado para el acceso directo.

Cuando se elimina un archivo de vínculo, el objeto correspondiente no se ve afectado.

Si crea un acceso directo a otro acceso directo, el sistema simplemente copia el archivo de vínculo en lugar de crear un nuevo archivo de vínculo. En este caso, los accesos directos no serán independientes entre sí.

Una aplicación puede registrar una extensión de nombre de archivo como un tipo de archivo de acceso directo. Si un archivo tiene una extensión de nombre de archivo que se ha registrado como un tipo de archivo de acceso directo, el sistema agrega automáticamente el icono de superposición de vínculo definido por el sistema (una flecha pequeña) al icono del archivo. Para registrar una extensión de nombre de archivo como un tipo de archivo de acceso directo, debe agregar el valor de IsShortcut a la descripción del registro de la extensión de nombre de archivo, tal como se muestra en el ejemplo siguiente. Tenga en cuenta que el shell debe reiniciarse para que el icono de superposición surta efecto. IsShortcut no tiene ningún valor de datos.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Nombres de acceso directo

El nombre del acceso directo, que es una cadena que aparece debajo del icono de vínculo de Shell, es en realidad el nombre del archivo del acceso directo. El usuario puede editar la cadena de Descripción seleccionándola y escribiendo una nueva cadena.

### <a name="location-of-shortcuts-in-the-namespace"></a>Ubicación de los accesos directos en el espacio de nombres

Puede existir un acceso directo en el escritorio o en cualquier lugar del espacio de nombres del shell. Del mismo modo, el objeto que está asociado al método abreviado también puede existir en cualquier parte del espacio de nombres del shell. Una aplicación puede usar el método [**IShellLink:: SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) para establecer la ruta de acceso y el nombre de archivo del objeto asociado, y el método [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) para recuperar la ruta de acceso y el nombre de archivo actuales del objeto.

### <a name="shortcut-working-directory"></a>Directorio de trabajo de acceso directo

El directorio de trabajo es el directorio en el que el objeto correspondiente de un acceso directo carga o almacena archivos cuando el usuario no identifica un directorio específico. Un archivo de vínculo contiene el nombre del directorio de trabajo para el objeto correspondiente. Una aplicación puede establecer el nombre del directorio de trabajo para el objeto correspondiente mediante el método [**IShellLink:: SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) y puede recuperar el nombre del directorio de trabajo actual para el objeto correspondiente mediante el método [**IShellLink:: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .

### <a name="shortcut-command-line-arguments"></a>Argumentos de la línea de comandos de acceso directo

Un archivo de vínculo contiene los argumentos de línea de comandos que el shell pasa al objeto correspondiente cuando el usuario selecciona el vínculo. Una aplicación puede establecer los argumentos de línea de comandos para un acceso directo mediante el método [**IShellLink:: SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) . Resulta útil establecer argumentos de la línea de comandos cuando la aplicación correspondiente, como un vinculador o un compilador, toma marcas especiales como argumentos. Una aplicación puede recuperar los argumentos de línea de comandos de un acceso directo mediante el método [**IShellLink:: GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .

### <a name="shortcut-show-commands"></a>Comandos de acceso directo para mostrar

Cuando el usuario hace doble clic en un acceso directo, el sistema inicia la aplicación asociada al objeto correspondiente y establece el estado de presentación inicial de la aplicación en función del comando show especificado por el acceso directo. El comando show puede ser cualquiera de los valores de SW \_ incluidos en la descripción de la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . Una aplicación puede establecer el comando show para un acceso directo mediante el método [**IShellLink:: SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) y puede recuperar el comando show actual mediante el método [**IShellLink:: GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .

### <a name="shortcut-icons"></a>Iconos de acceso directo

Al igual que otros objetos de Shell, un acceso directo tiene un icono. El usuario tiene acceso al objeto asociado a un acceso directo haciendo doble clic en el icono del acceso directo. Cuando el sistema crea un icono para un acceso directo, usa el mapa de bits del objeto correspondiente y agrega el icono de superposición de vínculo definido por el sistema (una flecha pequeña) a la esquina inferior izquierda. Una aplicación puede establecer la ubicación (ruta de acceso e índice) del icono de un acceso directo mediante el método [**IShellLink:: SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) . Una aplicación puede recuperar esta ubicación mediante el método [**IShellLink:: GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .

### <a name="shortcut-descriptions"></a>Descripciones de acceso directo

Los accesos directos tienen descripciones, pero el usuario nunca los ve. Una aplicación puede usar una descripción para almacenar cualquier información de texto. Las descripciones se establecen mediante el método [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) y se recuperan mediante el método [**IShellLink:: getDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .

### <a name="shortcut-keyboard-shortcuts"></a>Métodos abreviados de teclado de acceso directo

Un objeto de acceso directo puede tener asociado un método abreviado de teclado. Los métodos abreviados de teclado permiten al usuario presionar una combinación de teclas para activar un acceso directo. Una aplicación puede establecer el método abreviado de teclado para un acceso directo mediante el método [**IShellLink:: SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) y puede recuperar el método abreviado de teclado actual mediante el método [**IShellLink:: GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) .

### <a name="item-identifiers-and-identifier-lists"></a>Identificadores de elementos y listas de identificadores

El shell utiliza identificadores de objeto en el espacio de nombres del shell. Todos los objetos visibles en el Shell (archivos, directorios, servidores, grupos de trabajo, etc.) tienen identificadores únicos entre los objetos de su carpeta principal. Estos identificadores se denominan identificadores de elemento y tienen el tipo de datos [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , tal y como se define en el archivo de encabezado Shtypes. h. Un identificador de elemento es una secuencia de bytes de longitud variable que contiene información que identifica un objeto dentro de una carpeta. Solo el creador de un identificador de elemento conoce el contenido y el formato del identificador. La única parte de un identificador de elemento que usa el Shell son los primeros dos bytes, que especifican el tamaño del identificador.

Cada carpeta primaria tiene su propio identificador de elemento que la identifica dentro de su propia carpeta principal. Por lo tanto, cualquier objeto de Shell se puede identificar de forma única mediante una lista de identificadores de elemento. Una carpeta primaria mantiene una lista de identificadores para los elementos que contiene. La lista tiene el tipo de datos [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Las listas de identificadores de elementos se asignan mediante el Shell y se pueden pasar a través de interfaces de Shell, como [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder). Es importante recordar que cada identificador de una lista de identificadores de elementos solo es significativo dentro del contexto de su carpeta principal.

Una aplicación puede establecer la lista de identificadores de elementos de un acceso directo mediante el método [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) . Este método es útil cuando se establece un acceso directo a un objeto que no es un archivo, como una impresora o una unidad de disco. Una aplicación puede recuperar la lista de identificadores de elementos de un acceso directo mediante el método [**IShellLink:: GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .

## <a name="using-shell-links"></a>Usar vínculos de Shell

Esta sección contiene ejemplos que muestran cómo crear y resolver accesos directos desde una aplicación basada en Win32. En esta sección se da por supuesto que está familiarizado con la programación de Win32, C++ y OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Crear un acceso directo y un acceso directo a una carpeta en un archivo

En la función de ejemplo CreateLink del ejemplo siguiente se crea un acceso directo. Los parámetros incluyen un puntero al nombre del archivo al que se va a vincular, un puntero al nombre del acceso directo que está creando y un puntero a la descripción del vínculo. La descripción consta de la cadena "acceso directo a **nombre de archivo**", donde **nombre de archivo** es el nombre del archivo al que se va a vincular.

Para crear un acceso directo a una carpeta mediante la función de ejemplo CreateLink, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ FolderShortcut, en lugar de CLSID \_ ShellLink (CLSID \_ FolderShortcut admite IShellLink). El resto del código sigue siendo el mismo.

Dado que CreateLink llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , se supone que ya se ha llamado a la función [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . CreateLink usa la interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para guardar el acceso directo y la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para almacenar el nombre de archivo y la descripción.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Resolución de un acceso directo

Es posible que una aplicación necesite tener acceso y manipular un acceso directo creado previamente. Esta operación se conoce como resolver el acceso directo.

La función ResolveIt definida por la aplicación en el ejemplo siguiente resuelve un acceso directo. Sus parámetros incluyen un identificador de ventana, un puntero a la ruta de acceso del acceso directo y la dirección de un búfer que recibe la nueva ruta de acceso al objeto. El identificador de ventana identifica la ventana primaria para cualquier cuadro de mensaje que el shell pueda necesitar Mostrar. Por ejemplo, el shell puede mostrar un cuadro de mensaje si el vínculo está en medios no compartidos, si se producen problemas de red, si el usuario necesita insertar un disquete, etc.

La función ResolveIt llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y da por supuesto que ya se ha llamado a la función [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Tenga en cuenta que ResolveIt debe usar la interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para almacenar la información del vínculo. **IPersistFile** se implementa mediante el objeto [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) . La información del vínculo debe cargarse antes de que se recupere la información de la ruta de acceso, que se muestra más adelante en el ejemplo. Si no se carga la información de vínculo, se producirá un error en las llamadas a las funciones miembro [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) y [**IShellLink:: getDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Crear un acceso directo a un objeto que no es de archivo

Crear un acceso directo a un objeto que no es un archivo, como una impresora, es similar a crear un acceso directo a un archivo, salvo que en lugar de establecer la ruta de acceso en el archivo, debe establecer la lista de identificadores en la impresora. Para establecer la lista de identificadores, llame al método [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , especificando la dirección de una lista de identificadores.

Cada objeto del espacio de nombres del shell tiene un identificador de elemento. El shell suele concatenar los identificadores de elemento en listas terminadas en null que se componen de cualquier número de identificadores de elemento. Para obtener más información sobre los identificadores de elemento, vea [identificadores de elemento y listas de identificadores](#item-identifiers-and-identifier-lists).

En general, si tiene que establecer un acceso directo a un elemento que no tenga un nombre de archivo, como una impresora, ya tendrá un puntero a la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del objeto. **IShellFolder** se usa para crear extensiones de espacio de nombres.

Una vez que tenga el identificador de clase para [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), puede llamar a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar la dirección de la interfaz. Después, puede llamar a la interfaz para enumerar los objetos de la carpeta y recuperar la dirección del identificador de elemento para el objeto que está buscando. Por último, puede usar la dirección en una llamada a la función miembro [**IShellLink:: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) para crear un acceso directo al objeto.

 

 
