---
description: Un vínculo de Shell es un objeto de datos que contiene información que se usa para acceder a otro objeto del espacio de nombres del shell&8212; es decir, cualquier objeto visible a través de \# Windows Explorer.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Vínculos de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256989"
---
# <a name="shell-links"></a>Vínculos de shell

Un *vínculo de Shell* es un objeto de datos que contiene información que se usa para acceder a otro objeto en el espacio de nombres del shell, es decir, cualquier objeto visible a través de Windows Explorer. Los tipos de objetos a los que se puede acceder a través de vínculos de Shell incluyen archivos, carpetas, unidades de disco e impresoras. Un vínculo de Shell permite que un usuario o una aplicación accedan a un objeto desde cualquier lugar del espacio de nombres. El usuario o la aplicación no necesita conocer el nombre y la ubicación actuales del objeto.

-   [Acerca de los vínculos de Shell](#about-shell-links)
    -   [Resolución de vínculos](#link-resolution)
    -   [Archivos de vínculo](#link-files)
    -   [Identificadores de elementos y listas de identificadores](#item-identifiers-and-identifier-lists)
-   [Uso de vínculos de shell](#using-shell-links)
    -   [Crear un acceso directo y un acceso directo de carpeta a un archivo](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Resolver un acceso directo](#resolving-a-shortcut)
    -   [Crear un acceso directo a un objeto que no es de archivo](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Acerca de los vínculos de Shell

El usuario crea un vínculo de Shell eligiendo el comando **Crear** acceso directo en el menú contextual de un objeto. El sistema crea automáticamente un icono para el vínculo de Shell combinando el icono del objeto con una flecha pequeña (conocida como icono de superposición de vínculo definido por el sistema) que aparece en la esquina inferior izquierda del icono. Un vínculo de Shell que tiene un icono se denomina acceso directo; sin embargo, los términos vínculo y acceso directo de Shell se suelen usar indistintamente. Normalmente, el usuario crea accesos directos para obtener acceso rápido a los objetos almacenados en subcarpetas o en carpetas compartidas de otros equipos. Por ejemplo, un usuario puede crear un acceso directo a un documento Microsoft Word que se encuentra en una subcarpeta y colocar el icono de acceso directo en el escritorio. A continuación, el usuario puede abrir el documento haciendo doble clic en el icono de acceso directo. Si el documento se mueve o cambia de nombre después de crear el acceso directo, el sistema intentará actualizar el acceso directo la próxima vez que el usuario lo seleccione.

Las aplicaciones también pueden crear y usar vínculos y accesos directos de Shell. Por ejemplo, una aplicación de procesamiento de texto podría crear un vínculo de Shell para implementar una lista de los documentos usados más recientemente. Una aplicación crea un vínculo de Shell mediante la [**interfaz IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para crear un objeto de vínculo de Shell. La aplicación usa la [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) [**o IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) para almacenar el objeto en un archivo o secuencia.

> [!Note]  
> No puede usar [**IShellLink para**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) crear un vínculo a una dirección URL.

 

En esta introducción se describe la [**interfaz IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) y se explica cómo usarla para crear y resolver vínculos de Shell desde una aplicación basada en Microsoft Win32. Dado que el diseño de los vínculos de Shell se basa en el modelo de objetos de componentes OLE (COM), debe estar familiarizado con los conceptos básicos de la programación COM y OLE antes de leer esta introducción.

### <a name="link-resolution"></a>Resolución de vínculos

Si un usuario crea un acceso directo a un objeto y el nombre o la ubicación del objeto se cambia más adelante, el sistema realiza automáticamente los pasos para actualizar o resolver el acceso directo la próxima vez que el usuario lo seleccione. Sin embargo, si una aplicación crea un vínculo de Shell y lo almacena en una secuencia, el sistema no intenta resolver automáticamente el vínculo. La aplicación debe resolver el vínculo llamando al [**método IShellLink::Resolve.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)

Cuando se crea un vínculo de Shell, el sistema guarda información sobre el vínculo. Al resolver un vínculo, ya sea automáticamente o con una llamada [**AShellLink::Resolve,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) el sistema recupera primero la ruta de acceso asociada al vínculo de Shell mediante un puntero a la lista de identificadores del vínculo de Shell. Para obtener más información sobre la lista de identificadores, vea [Identificadores de elemento y Listas de identificadores](#item-identifiers-and-identifier-lists). El sistema busca el objeto asociado en esa ruta de acceso y, si encuentra el objeto, resuelve el vínculo. Si el sistema no encuentra el objeto, llama a en el servicio [Distributed Link Tracking and Object Identifiers](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT), si está disponible, para buscar el objeto. Si el servicio DLT no está disponible o no encuentra el objeto, el sistema busca en el mismo directorio un objeto con la misma hora y atributos de creación de archivos, pero con un nombre diferente. Este tipo de búsqueda resuelve un vínculo a un objeto cuyo nombre ha cambiado.

Si el sistema sigue sin encontrar el objeto, busca en los directorios, el escritorio y los volúmenes locales, buscando recursivamente en el árbol de directorios un objeto con el mismo nombre o la misma hora de creación. Si el sistema sigue sin encontrar una coincidencia, muestra un cuadro de diálogo en el que se solicita al usuario una ubicación. Una aplicación puede suprimir el cuadro de diálogo especificando el valor de la interfaz de usuario **\_ SLR \_ NO** en una llamada a [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Inicialización de la biblioteca de objetos componentes

Para que una aplicación pueda crear y resolver accesos directos, debe inicializar la biblioteca de objetos de componente mediante una llamada a [**la función CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize) Cada llamada a **CoInitialize** requiere una llamada correspondiente a la función [**CoUninitialize,**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) a la que una aplicación debe llamar cuando finaliza. La llamada a **CoUninitialize** garantiza que la aplicación no finalice hasta que haya recibido todos sus mensajes pendientes.

### <a name="location-independent-names"></a>Location-Independent nombres

El sistema proporciona nombres independientes de la ubicación para los vínculos de Shell a objetos almacenados en carpetas compartidas. Si el objeto se almacena localmente, el sistema proporciona la ruta de acceso local y el nombre de archivo para el objeto. Si el objeto se almacena de forma remota, el sistema proporciona un nombre de recurso de red UNC (Convención de nomenclatura universal) para el objeto. Dado que el sistema proporciona nombres independientes de la ubicación, un vínculo de Shell puede actuar como un nombre universal para un archivo que se puede transferir a otros equipos.

### <a name="link-files"></a>Archivos de vínculo

Cuando el usuario crea un acceso directo  a un objeto eligiendo el comando Crear acceso directo en el menú contextual del objeto, Windows almacena la información que necesita para acceder al objeto en un archivo de vínculo, un archivo binario que tiene la extensión de nombre de archivo .lnk. Un archivo de vínculo contiene la siguiente información:

-   Ubicación (ruta de acceso) del objeto al que hace referencia el acceso directo (denominado objeto correspondiente).
-   Directorio de trabajo del objeto correspondiente.
-   Lista de argumentos que el sistema pasa al objeto correspondiente cuando se activa el método [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) para el acceso directo.
-   El comando show usado para establecer el estado de presentación inicial del objeto correspondiente. Este es uno de los valores de SW \_ descritos en [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   Ubicación (ruta de acceso e índice) del icono del acceso directo.
-   Cadena de descripción del acceso directo.
-   Método abreviado de teclado para el acceso directo.

Cuando se elimina un archivo de vínculo, el objeto correspondiente no se ve afectado.

Si crea un acceso directo a otro acceso directo, el sistema simplemente copia el archivo de vínculo en lugar de crear un nuevo archivo de vínculo. En este caso, los accesos directos no serán independientes entre sí.

Una aplicación puede registrar una extensión de nombre de archivo como un tipo de archivo de acceso directo. Si un archivo tiene una extensión de nombre de archivo que se ha registrado como un tipo de archivo de acceso directo, el sistema agrega automáticamente el icono de superposición de vínculo definido por el sistema (una flecha pequeña) al icono del archivo. Para registrar una extensión de nombre de archivo como un tipo de archivo de acceso directo, debe agregar el valor IsShortcut a la descripción del Registro de la extensión de nombre de archivo, como se muestra en el ejemplo siguiente. Tenga en cuenta que el shell debe reiniciarse para que el icono de superposición suba efecto. IsShortcut no tiene ningún valor de datos.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Nombres de acceso directo

El nombre del acceso directo, que es una cadena que aparece debajo del icono de vínculo shell, es realmente el nombre de archivo del propio acceso directo. El usuario puede editar la cadena de descripción seleccionándose y especificando una nueva cadena.

### <a name="location-of-shortcuts-in-the-namespace"></a>Ubicación de los accesos directos en el espacio de nombres

Puede existir un acceso directo en el escritorio o en cualquier lugar del espacio de nombres del shell. De forma similar, el objeto asociado al acceso directo también puede existir en cualquier lugar del espacio de nombres del shell. Una aplicación puede usar el método [**IShellLink::SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) para establecer la ruta de acceso y el nombre de archivo para el objeto asociado, y el método [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) para recuperar la ruta de acceso actual y el nombre de archivo del objeto.

### <a name="shortcut-working-directory"></a>Directorio de trabajo de acceso directo

El directorio de trabajo es el directorio donde el objeto correspondiente de un acceso directo carga o almacena archivos cuando el usuario no identifica un directorio específico. Un archivo de vínculo contiene el nombre del directorio de trabajo para el objeto correspondiente. Una aplicación puede establecer el nombre del directorio de trabajo para el objeto correspondiente mediante el método [**IShellLink::SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) y puede recuperar el nombre del directorio de trabajo actual para el objeto correspondiente mediante el método [**IShellLink::GetWorkingDirectory.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory)

### <a name="shortcut-command-line-arguments"></a>Argumentos de la línea de comandos de acceso directo

Un archivo de vínculo contiene argumentos de línea de comandos que el Shell pasa al objeto correspondiente cuando el usuario selecciona el vínculo. Una aplicación puede establecer los argumentos de la línea de comandos para un acceso directo mediante el método [**IShellLink::SetArguments.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) Resulta útil establecer argumentos de línea de comandos cuando la aplicación correspondiente, como un vinculador o compilador, toma marcas especiales como argumentos. Una aplicación puede recuperar los argumentos de la línea de comandos de un acceso directo mediante el método [**IShellLink::GetArguments.**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments)

### <a name="shortcut-show-commands"></a>Comandos para mostrar accesos directos

Cuando el usuario hace doble clic en un acceso directo, el sistema inicia la aplicación asociada al objeto correspondiente y establece el estado de presentación inicial de la aplicación en función del comando show especificado por el acceso directo. El comando show puede ser cualquiera de los valores sw \_ incluidos en la descripción de la [**función ShowWindow.**](/windows/win32/api/winuser/nf-winuser-showwindow) Una aplicación puede establecer el comando show para un acceso directo mediante el método [**IShellLink::SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) y puede recuperar el comando show actual mediante el método [**IShellLink::GetShowCmd.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd)

### <a name="shortcut-icons"></a>Iconos de acceso directo

Al igual que otros objetos de Shell, un acceso directo tiene un icono. El usuario accede al objeto asociado a un acceso directo haciendo doble clic en el icono del acceso directo. Cuando el sistema crea un icono para un acceso directo, usa el mapa de bits del objeto correspondiente y agrega el icono de superposición de vínculo definido por el sistema (una flecha pequeña) a la esquina inferior izquierda. Una aplicación puede establecer la ubicación (ruta de acceso e índice) del icono de un acceso directo mediante el método [**IShellLink::SetIconLocation.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) Una aplicación puede recuperar esta ubicación mediante el [**método IShellLink::GetIconLocation.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation)

### <a name="shortcut-descriptions"></a>Descripciones de accesos directos

Los accesos directos tienen descripciones, pero el usuario nunca los ve. Una aplicación puede usar una descripción para almacenar cualquier información de texto. Las descripciones se establecen mediante el método [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) y se recuperan mediante el [**método IShellLink::GetDescription.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription)

### <a name="shortcut-keyboard-shortcuts"></a>Métodos abreviados de teclado

Un objeto de método abreviado puede tener asociado un método abreviado de teclado. Los métodos abreviados de teclado permiten al usuario presionar una combinación de teclas para activar un acceso directo. Una aplicación puede establecer el método abreviado de teclado para un acceso directo mediante el método [**IShellLink::SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) y puede recuperar el método abreviado de teclado actual mediante el método [**IShellLink::GetHotkey.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey)

### <a name="item-identifiers-and-identifier-lists"></a>Identificadores de elementos y listas de identificadores

El Shell usa identificadores de objeto dentro del espacio de nombres del shell. Todos los objetos visibles en el Shell (archivos, directorios, servidores, grupos de trabajo, entre otros) tienen identificadores únicos entre los objetos dentro de su carpeta primaria. Estos identificadores se denominan identificadores de elemento, y tienen el tipo de datos [**DESCIMED**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) tal y como se define en el archivo de encabezado Shtypes.h. Un identificador de elemento es una secuencia de bytes de longitud variable que contiene información que identifica un objeto dentro de una carpeta. Solo el creador de un identificador de elemento conoce el contenido y el formato del identificador. La única parte de un identificador de elemento que usa el Shell son los dos primeros bytes, que especifican el tamaño del identificador.

Cada carpeta primaria tiene su propio identificador de elemento que la identifica dentro de su propia carpeta primaria. Por lo tanto, cualquier objeto shell se puede identificar de forma única mediante una lista de identificadores de elemento. Una carpeta primaria mantiene una lista de identificadores para los elementos que contiene. La lista tiene el tipo [**de datos ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) El shell asigna listas de identificadores de elementos y se pueden pasar a través de interfaces de Shell, como [**IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Es importante recordar que cada identificador de una lista de identificadores de elemento solo es significativo dentro del contexto de su carpeta primaria.

Una aplicación puede establecer una lista de identificadores de elemento de un acceso directo mediante el [**método IShellLink::SetIDList.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) Este método es útil al establecer un acceso directo a un objeto que no es un archivo, como una impresora o una unidad de disco. Una aplicación puede recuperar la lista de identificadores de elementos de un acceso directo mediante el [**método IShellLink::GetIDList.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist)

## <a name="using-shell-links"></a>Uso de vínculos de shell

Esta sección contiene ejemplos que muestran cómo crear y resolver accesos directos desde una aplicación basada en Win32. En esta sección se supone que está familiarizado con la programación win32, C++ y OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Crear un acceso directo y un acceso directo de carpeta a un archivo

La función de ejemplo CreateLink del ejemplo siguiente crea un acceso directo. Los parámetros incluyen un puntero al nombre del archivo al que se va a vincular, un puntero al nombre del acceso directo que está creando y un puntero a la descripción del vínculo. La descripción consta de la cadena "Acceso directo al nombre de archivo **",** donde **nombre** de archivo es el nombre del archivo al que se va a vincular.

Para crear un acceso directo de carpeta mediante la función de ejemplo CreateLink, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mediante CLSID FolderShortcut, en lugar de \_ CLSID \_ ShellLink (CLSID \_ FolderShortcut admite IShellLink). El resto del código sigue siendo el mismo.

Dado que CreateLink llama a [**la función CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) se supone que ya se ha llamado a la función [**CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize) CreateLink usa la [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para guardar el acceso directo y la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para almacenar el nombre de archivo y la descripción.


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



### <a name="resolving-a-shortcut"></a>Resolver un acceso directo

Es posible que una aplicación tenga que acceder y manipular un acceso directo que se creó anteriormente. Esta operación se conoce como resolución del acceso directo.

La función ResolveIt definida por la aplicación en el ejemplo siguiente resuelve un acceso directo. Sus parámetros incluyen un identificador de ventana, un puntero a la ruta de acceso del acceso directo y la dirección de un búfer que recibe la nueva ruta de acceso al objeto. El identificador de ventana identifica la ventana primaria para los cuadros de mensaje que el Shell puede necesitar mostrar. Por ejemplo, shell puede mostrar un cuadro de mensaje si el vínculo está en medios no compartidos, si se producen problemas de red, si el usuario necesita insertar un disquete, y así sucesivamente.

La función ResolveIt llama a [**la función CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y supone que ya se ha llamado a la función [**CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize) Tenga en cuenta que ResolveIt debe usar la [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para almacenar la información del vínculo. El objeto [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) implementa **IPersistFile.** La información del vínculo debe cargarse antes de recuperar la información de ruta de acceso, que se muestra más adelante en el ejemplo. Si no se carga la información del vínculo, se producirá un error en las llamadas a las funciones miembro [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) e [**IShellLink::GetDescription.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription)


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

La creación de un acceso directo a un objeto que no es de archivo, como una impresora, es similar a crear un acceso directo a un archivo, salvo que, en lugar de establecer la ruta de acceso al archivo, debe establecer la lista de identificadores en la impresora. Para establecer la lista de identificadores, llame al método [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) y especifique la dirección de una lista de identificadores.

Cada objeto dentro del espacio de nombres del shell tiene un identificador de elemento. El Shell a menudo concatena los identificadores de elemento en listas terminadas en NULL que constan de cualquier número de identificadores de elemento. Para obtener más información sobre los identificadores de elemento, vea [Identificadores de elemento y Listas de identificadores](#item-identifiers-and-identifier-lists).

En general, si necesita establecer un acceso directo a un elemento que no tiene un nombre de archivo, como una impresora, ya tendrá un puntero a la interfaz [**IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) objeto. **IShellFolder se** usa para crear extensiones de espacio de nombres.

Una vez que tenga el identificador de clase para [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)puede llamar a la [**función CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar la dirección de la interfaz. A continuación, puede llamar a la interfaz para enumerar los objetos de la carpeta y recuperar la dirección del identificador de elemento para el objeto que está buscando. Por último, puede usar la dirección en una llamada a la función miembro [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) para crear un acceso directo al objeto .

 

 
