---
description: En esta sección se describe cómo agregar cadenas de recursos a la tabla de accesos directos Windows Installer para su uso con las interfaces de usuario multilingüe (MUI).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Un ejemplo de método abreviado de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652633"
---
# <a name="a-mui-shortcut-example"></a>Un ejemplo de método abreviado de MUI

En esta sección se describe cómo agregar cadenas de recursos a la tabla de [accesos directos](shortcut-table.md) Windows Installer para su uso con las interfaces de usuario multilingüe (MUI).

**Windows Installer 2,0 y Windows Installer 3,0:** No compatible. Este ejemplo requiere Windows Installer 4,0.

Consulte la documentación de la [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface) para obtener información sobre cómo desarrollar aplicaciones habilitadas para MUI.

Para agregar las cadenas de recursos que usan las interfaces de usuario multilingüe de Windows Vista a un paquete de Windows Installer:

1.  Agregue la información de todos los archivos de idioma y de idioma neutro a la [tabla de archivos](file-table.md). Por ejemplo, los archivos pueden constar de un archivo independiente del idioma (msimsg.dll) y archivos de idioma para inglés (msimsgen.dll. MUI), Japonés (msimsgja.dll. MUI) y chino (msimsgcs.dll. MUI). Cada archivo puede pertenecer a un componente diferente. Cada archivo puede tener un nombre de archivo largo y corto. En el caso de este ejemplo, se puede Agregar la siguiente información a la [tabla de archivos](file-table.md).

    [Tabla de archivos](file-table.md) (parcial)

    

    | Archivo        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ mui \_ ja | msimsgja.dll\|msimsg.dll. MUI |
    | msimsgmuics | MSIMSG \_ mui \_ CS | msimsgcs.dll\|msimsg.dll. MUI |
    | msimsgmuien | MSIMSG \_ mui \_ en | msimsgen.dll\|msimsg.dll. MUI |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Agregue información a la [tabla de componentes](component-table.md) de estos componentes. Cada componente tiene un identificador GUID único que debe especificarse en el campo ComponentId de la tabla de componentes. El archivo que pertenece al componente puede actuar como la ruta de acceso de ese componente. El directorio que contiene cada componente se puede especificar en el \_ campo directorio. La siguiente información se puede Agregar a la tabla de componentes.

    [Tabla de componentes](component-table.md) (parcial)

    

    | Componente       | Directorio\_   | Rutas     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ mui \_ ja | MUIFolder \_ ja | msimsgmuija |
    | MSIMSG \_ mui \_ CS | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ mui \_ en | MUIFolder \_ en | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Edite la tabla del [directorio](directory-table.md) para que los componentes se instalen en los directorios correctos. Asegúrese de incluir información sobre el directorio en el que se instalará el acceso directo. Por ejemplo, la siguiente información puede agregarse a la tabla de directorio de un paquete que instala los componentes de y un acceso directo ubicado en el directorio DesktopFolder.

    [Tabla de directorio](directory-table.md) (parcial)

    

    | Directorio     | Directorio \_ primario | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | MUIFolder     | MsiTest           | LINGÜE        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ en | MUIFolder         | es-ES      |
    | MUIFolder \_ ja | MUIFolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  Agregue una fila a la tabla de [accesos directos](shortcut-table.md) para cada acceso directo. Por ejemplo, la tabla de [acceso directo](shortcut-table.md) podría contener la siguiente información para dos métodos abreviados, Quick1 y Quick2, instalados en el directorio DirectoryFolder Cada acceso directo pertenece a la característica especificada en el campo de destino. El icono asociado con el acceso directo se puede especificar en el \_ campo icono y en la tabla de [iconos](icon-table.md) .

    [Tabla de acceso directo](shortcut-table.md) (parcial)

    

    | Acceso directo | Directorio\_   | Componente\_ | Destino               | Icono             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |

    

     

5.  Agregue información a la tabla de la [tabla de características](feature-table.md) para la característica a la que pertenece el acceso directo. Cuando se activa el acceso directo, el instalador comprueba que todos los componentes que pertenecen a esta característica se instalan antes de iniciar el archivo de clave del componente especificado en la \_ columna componente de la tabla de [accesos directos](shortcut-table.md) . En el caso de este ejemplo, se puede Agregar la siguiente información a la tabla de la tabla de características para la \_ característica local FeatureParent1.

    [Tabla de características](feature-table.md) (parcial)

    

    | Característica               | Característica \_ principal       | Title                 | Atributos |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ local |                       | FeatureParent1 \_ local | 16         |
    | FeatureChild1 \_ local  | FeatureParent1 \_ local | FeatureParent1 \_ local | 0          |

    

     

6.  Para cada nuevo acceso directo, agregue la información de la cadena de recursos a los campos DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL y DescriptionResourceId de la [tabla de acceso directo](shortcut-table.md). Los campos DisplayResourceDLL y DescriptionResourceDLL contienen la cadena de recursos en formato de cadena [con formato](formatted.md) . La cadena con formato puede utilizar la \[ \# Convención *filekey* \] del formato [con formato](formatted.md) . Agregue los índices de presentación y descripción para las cadenas de recursos en los campos DisplayResourceId y DescriptionResourceId.

    [Tabla de acceso directo](shortcut-table.md) (parcial)

    

    | Acceso directo | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Después de instalar el paquete, pruebe para asegurarse de que la interfaz de usuario multilingüe funciona según lo previsto.

 

 
