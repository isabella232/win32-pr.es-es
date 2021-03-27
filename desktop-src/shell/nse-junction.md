---
description: La raíz de una extensión de espacio de nombres se muestra normalmente en el explorador de Windows como una carpeta en las vistas de árbol y de carpeta.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910778"
---
# <a name="specifying-a-namespace-extensions-location"></a>Especificar la ubicación de una extensión de espacio de nombres

La raíz de una extensión de espacio de nombres se muestra normalmente en el explorador de Windows como una carpeta en las vistas de árbol y de carpeta. Para que el explorador de Windows muestre los archivos y subcarpetas de la extensión, debe especificar dónde se encuentra la carpeta raíz en la jerarquía del espacio de nombres del shell. Esta ubicación se conoce como punto de *Unión*.

-   [Usar carpetas virtuales como puntos de Unión](#using-virtual-folders-as-junction-points)
-   [Usar carpetas del sistema de archivos como puntos de Unión](#using-file-system-folders-as-junction-points)
-   [Abrir una vista de una extensión de espacio de nombres](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Usar carpetas virtuales como puntos de Unión

La manera más sencilla de definir el punto de unión de una extensión es convertir la carpeta raíz en una subcarpeta de una carpeta virtual del sistema. Este tipo de punto de Unión se conoce como *punto de Unión virtual*. Las carpetas **Desktop** y **mi PC** son las ubicaciones típicas de los puntos de Unión virtuales, pero también puede definir un punto de Unión virtual en un equipo remoto o en las carpetas **mis sitios de red**, **Internet Explorer** y **Panel de control** .

Para definir un punto de Unión virtual, cree una subclave de la clave que represente la carpeta virtual adecuada y asígnele el nombre de la forma de cadena del identificador de clase (CLSID) de la extensión. El CLSID registrado aparecería de la siguiente manera.

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

El nombre de la *carpeta virtual* es una de las subclaves de la tabla siguiente.



| Ubicación          | Nombre de carpeta virtual                        |
|-------------------|--------------------------------------------|
| Panel de control     | **ControlPanel**                           |
| Escritorio           | **Dispositivo de escritorio**                                |
| Red completa    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Mi PC       | **MyComputer**                             |
| Mis sitios de red | **NetworkNeighborhood**                    |
| Equipo remoto   | **Equiporemoto**                         |
| Archivos de usuarios       | **UsersFiles**                             |



 

Las extensiones remotas se deben inicializar con [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Usar carpetas del sistema de archivos como puntos de Unión

Hay dos maneras de definir carpetas del sistema de archivos como puntos de Unión. El enfoque más sencillo consiste en crear una carpeta en la ubicación adecuada y anexar un punto al nombre de la carpeta, seguido de la forma de cadena del CLSID de la extensión. Solo el nombre de la carpeta será visible en el explorador de Windows. En el ejemplo siguiente se crea un punto de unión con un nombre para mostrar de mi carpeta.


```
MyFolder.{Extension CLSID}
```



Como alternativa, puede definir una carpeta con el nombre convencional como punto de Unión:

-   Crear la carpeta de solo lectura.
-   Convertir la carpeta en una carpeta del sistema mediante una llamada a [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Colocar un archivo de Desktop.ini oculto en la carpeta que incluye el CLSID de la extensión.

Desktop.ini es un archivo de texto estándar que se puede Agregar a cualquier carpeta para personalizar determinados aspectos del comportamiento de la carpeta. Para obtener una explicación general sobre cómo usar este archivo, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Para definir una carpeta como punto de Unión, el \[ . \] La sección ShellClassInfo de Desktop.ini debe contener el CLSID de la extensión como se indica a continuación:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Abrir una vista de una extensión de espacio de nombres

Cuando un usuario examina un punto de Unión, el explorador de Windows crea automáticamente una vista de la carpeta raíz. También puede crear una vista mediante el inicio explícito de Explorer.exe con el CLSID de la extensión como argumento. Por ejemplo, puede usar este enfoque para iniciar una vista de una extensión desde un menú contextual o un acceso directo. Por ejemplo, para iniciar una vista de una extensión que incluye una vista de árbol, puede utilizar la siguiente cadena de comandos.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Se puede usar una cadena de comandos alternativa para iniciar una vista de un objeto dentro de la extensión. Esta característica sería útil, por ejemplo, para una extensión que utiliza una vista de carpeta para permitir que los usuarios vean el contenido de uno de varios archivos comprimidos.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



El parámetro *objectname* es el nombre del objeto que se va a ver. El explorador de Windows convierte el nombre en su PIDL correspondiente y pasa el PIDL al método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) del objeto de la nueva carpeta.

> [!Note]  
> La cadena CLSID debe ir precedida de un par de dos puntos (::) o se producirá un error en el comando. La marca de barra diagonal-e (/e) utilizada en las dos líneas de comandos de ejemplo mostradas anteriormente indica al explorador de Windows que muestre una vista de árbol. La marca se debe separar entre los dos dos puntos mediante una coma. Si no desea una vista de árbol, omita la marca/e y la coma.

 

 

 



