---
description: Normalmente, el Explorador de Windows muestra la raíz de una extensión de espacio de nombres como una carpeta en las vistas de árbol y carpeta.
title: Especificar la ubicación de una extensión de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361044"
---
# <a name="specifying-a-namespace-extensions-location"></a>Especificar la ubicación de una extensión de espacio de nombres

Normalmente, el Explorador de Windows muestra la raíz de una extensión de espacio de nombres como una carpeta en las vistas de árbol y carpeta. Para Windows explorer muestre los archivos y subcarpetas de la extensión, debe especificar dónde se encuentra la carpeta raíz en la jerarquía de espacios de nombres de Shell. Esta ubicación se conoce como punto *de unión.*

-   [Usar carpetas virtuales como puntos de unión](#using-virtual-folders-as-junction-points)
-   [Usar carpetas del sistema de archivos como puntos de unión](#using-file-system-folders-as-junction-points)
-   [Abrir una vista de una extensión de espacio de nombres](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Usar carpetas virtuales como puntos de unión

La manera más sencilla de definir el punto de unión de una extensión es convertir la carpeta raíz en una subcarpeta de una carpeta virtual del sistema. Este tipo de punto de unión se conoce como punto *de unión virtual.* Las  carpetas Escritorio y **Mi PC** son las ubicaciones típicas de los puntos de unión virtuales, pero también puede definir un punto de unión virtual en un equipo remoto o en las carpetas Mis lugares de red **,** **Internet Explorer** **y Panel de control** virtuales.

Para definir un punto de unión virtual, cree una subclave de la clave que represente la carpeta virtual adecuada y asíéquela con el formato de cadena del identificador de clase (CLSID) de la extensión. El CLSID registrado aparecería como se muestra a continuación.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

*Nombre de carpeta* virtual es una de las subclaves de la tabla siguiente.



| Location          | Nombre de la carpeta virtual                        |
|-------------------|--------------------------------------------|
| Panel de control     | **Controlpanel**                           |
| Escritorio           | **Dispositivo de escritorio**                                |
| Red completa    | **NetworkNeighborigh** \\ **EntireNetwork** |
| Mi PC       | **Miequipo**                             |
| Mis sitios de red | **NetworkNeighborigh**                    |
| Equipo remoto   | **RemoteComputer**                         |
| Archivos de usuarios       | **UsersFiles**                             |



 

Las extensiones remotas se deben inicializar [**con IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Usar carpetas del sistema de archivos como puntos de unión

Hay dos maneras de definir carpetas del sistema de archivos como puntos de unión. El enfoque más sencillo es crear una carpeta en la ubicación adecuada y anexar un punto al nombre de la carpeta, seguido de la forma de cadena del CLSID de la extensión. Solo el nombre de la carpeta estará visible en Windows Explorador. En el ejemplo siguiente se crea un punto de unión con el nombre para mostrar MyFolder.


```
MyFolder.{Extension CLSID}
```



Como alternativa, puede definir una carpeta con nombre convencional como punto de unión mediante:

-   Convertir la carpeta en de solo lectura.
-   Convertir la carpeta en una carpeta del sistema mediante [**una llamada a PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Colocar un archivo Desktop.ini en la carpeta que incluye el CLSID de la extensión.

Desktop.ini es un archivo de texto estándar que se puede agregar a cualquier carpeta para personalizar determinados aspectos del comportamiento de la carpeta. Para obtener una explicación general de cómo usar este archivo, vea [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Para definir una carpeta como punto de unión, \[ . La sección ShellClassInfo de Desktop.ini debe contener el CLSID de la extensión \] como se muestra a continuación:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Abrir una vista de una extensión de espacio de nombres

Cuando un usuario navega a un punto de unión, Windows Explorer crea automáticamente una vista de la carpeta raíz. También puede crear una vista iniciando explícitamente Explorer.exe con el CLSID de la extensión como argumento. Por ejemplo, puede usar este enfoque para iniciar una vista de una extensión desde un menú contextual o un acceso directo. Por ejemplo, para iniciar una vista de MyExtension que incluye una vista de árbol, puede usar la siguiente cadena de comando.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Se puede usar una cadena de comando alternativa para iniciar una vista de un objeto dentro de la extensión. Esta característica sería útil, por ejemplo, para una extensión que usa una vista de carpeta para permitir a los usuarios ver el contenido de uno de varios archivos comprimidos.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



El *parámetro objectname* es el nombre del objeto que se va a ver. Windows El Explorador convierte el nombre en su PIDL correspondiente y pasa el PIDL al método [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) del nuevo objeto de carpeta.

> [!Note]  
> La cadena CLSID debe ir precedida de un par de dos puntos (::) o se producirá un error en el comando. La marca slash-e (/e) usada en las dos líneas de comandos de ejemplo mostradas anteriormente indica a Windows Explorer que muestre una vista de árbol. La marca debe estar separada de los dos puntos por una coma. Si no desea una vista de árbol, omita la marca /e y la coma.

 

 

 



