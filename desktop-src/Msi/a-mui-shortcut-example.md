---
description: En esta sección se describe cómo agregar cadenas de recursos a la tabla de accesos directos Windows Installer para su uso con interfaces de usuario multilingües (MUI).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Un ejemplo de acceso directo de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159273"
---
# <a name="a-mui-shortcut-example"></a>Un ejemplo de acceso directo de MUI

En esta sección se describe cómo agregar cadenas de recursos a la tabla de accesos directos Windows [Installer](shortcut-table.md) para su uso con interfaces de usuario multilingües (MSI).

**Windows Installer 2.0 y Windows Installer 3.0:** No se admite. Este ejemplo requiere Windows Installer 4.0.

Consulte la documentación [de Interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface) para obtener información sobre cómo desarrollar aplicaciones habilitadas para MUI.

Para agregar las cadenas de recursos que usa Windows interfaces de usuario multilingües de Vista a un paquete Windows Installer:

1.  Agregue la información de todos los archivos de idioma neutros y de idioma a la [tabla de archivos](file-table.md). Por ejemplo, los archivos pueden constar de un archivo con idioma neutro (msimsg.dll) y archivos de idioma para inglés (msimsgen.dll.mui), japonés (msimsgja.dll.mui) y chino (msimsgcs.dll.mui). Cada archivo puede pertenecer a un componente diferente. Cada archivo puede tener un nombre de archivo largo y corto. En el caso de este ejemplo, se puede agregar la siguiente información a la [tabla de archivos](file-table.md).

    [Tabla de archivos](file-table.md) (parcial)

    

    | Archivo        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MSIG MSI \_ JA | msimsgja.dll\|msimsg.dll.mui |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll.mui |
    | msimsgmuien | MSIMSG \_ MSIG MSI \_ EN | msimsgen.dll\|msimsg.dll.mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Agregue información a la [tabla Component para](component-table.md) estos componentes. Cada componente tiene un identificador GUID único que se debe especificar en el campo ComponentId de la tabla Component. El archivo que pertenece al componente puede actuar como KeyPath para ese componente. El directorio que contiene cada componente se puede especificar en el campo \_ Directorio. La siguiente información se puede agregar a la tabla Component.

    [Tabla de componentes](component-table.md) (parcial)

    

    | Componente       | Directorio\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MSIG MSI \_ JA | FOLDERFolder \_ JA | msimsgmuija |
    | MSIMSG \_ MUI \_ CS | CS deFOLDERFolder \_ | msimsgmuics |
    | MSIMSG \_ MSIG MSI \_ EN | FOLDERFolder \_ EN | msimsgmuien |
    | MSIMSG          | FOLDERFolder     | msimsgdll   |

    

     

3.  Edite [la tabla](directory-table.md) Directory para que los componentes se instalen en los directorios correctos. Asegúrese de incluir información sobre el directorio donde se instalará el acceso directo. Por ejemplo, se podría agregar la siguiente información a la tabla Directory de un paquete que instala los componentes y un acceso directo ubicado en el directorio DesktopFolder.

    [Tabla de directorios](directory-table.md) (parcial)

    

    | Directorio     | Elemento primario \_ del directorio | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | FOLDERFolder     | MsiTest           | MUI        |
    | CS deFOLDERFolder \_ | FOLDERFolder         | cs-CZ      |
    | FOLDERFolder \_ EN | FOLDERFolder         | es-ES      |
    | FOLDERFolder \_ JA | FOLDERFolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  Agregue una fila a la tabla [Acceso directo](shortcut-table.md) para cada acceso directo. Por ejemplo, la tabla [Acceso](shortcut-table.md) directo podría contener la siguiente información para dos accesos directos, Quick1 y Quick2, instalados en el directorio DirectoryFolder. Cada acceso directo pertenece a la característica especificada en el campo Destino. El icono asociado al acceso directo se puede especificar en el campo Icono \_ y en la tabla [Icono.](icon-table.md)

    [Tabla de métodos abreviados](shortcut-table.md) (parcial)

    

    | Acceso directo | Directorio\_   | Componente\_ | Destino               | Icono             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |

    

     

5.  Agregue información a la tabla [tabla de](feature-table.md) características a la que pertenece el acceso directo propietario de la característica. Cuando se activa el acceso directo, el instalador comprueba que todos los componentes que pertenecen a esta característica están instalados antes de iniciar el archivo de clave del componente especificado en la columna Componente de la tabla \_ [Acceso](shortcut-table.md) directo. En el caso de este ejemplo, se puede agregar la siguiente información a la tabla de características de la característica Local \_ FeatureParent1.

    [Tabla de características](feature-table.md) (parcial)

    

    | Característica               | Elemento \_ primario de la característica       | Título                 | Atributos |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ Local |                       | FeatureParent1 \_ Local | 16         |
    | FeatureChild1 \_ Local  | FeatureParent1 \_ Local | FeatureParent1 \_ Local | 0          |

    

     

6.  Para cada nuevo acceso directo, agregue la información de la cadena de recursos a los campos DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL y DescriptionResourceId de la tabla [Shortcut](shortcut-table.md). Los campos DisplayResourceDLL y DescriptionResourceDLL contienen la cadena de recurso en [el formato de cadena](formatted.md) con formato. La cadena con formato puede usar la convención \[ \# *filekey* \] del formato [Formatted.](formatted.md) Agregue los índices de visualización y descripción de las cadenas de recursos en los campos DisplayResourceId y DescriptionResourceId.

    [Tabla de métodos abreviados](shortcut-table.md) (parcial)

    

    | Acceso directo | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Después de instalar el paquete, pruebe para asegurarse de que el Interfaz de usuario multilingüe funciona según lo previsto.

 

 
