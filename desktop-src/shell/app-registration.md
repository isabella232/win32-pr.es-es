---
description: En este tema se describe el modo en que las aplicaciones pueden exponer información sobre ellos mismos necesarios para habilitar determinados escenarios.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registro de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000991"
---
# <a name="application-registration"></a>Registro de la aplicación

En este tema se describe el modo en que las aplicaciones pueden exponer información sobre ellos mismos necesarios para habilitar determinados escenarios. Esto incluye la información necesaria para localizar la aplicación, los verbos que admite la aplicación y los tipos de archivos que puede controlar una aplicación.

Este tema se organiza de la siguiente manera:

-   [Buscar un archivo ejecutable de aplicación](#finding-an-application-executable)
-   [Registro de aplicaciones](#registering-applications)
    -   [Usar la subclave de rutas de acceso de la aplicación](#using-the-app-paths-subkey)
    -   [Usar la subclave Applications](#using-the-applications-subkey)
-   [Registrar verbos y otra información de Asociación de archivos](#registering-verbs-and-other-file-association-information)
-   [Registrar un tipo percibido](#registering-a-perceived-type)
-   [Temas relacionados](#related-topics)

> [!Note]  
> Las aplicaciones también pueden registrarse en las aplicaciones configurar el acceso y los valores predeterminados del equipo (SPAD) y establecer programas predeterminados (SYDP) del panel de control. Para obtener información acerca del registro de aplicaciones de SPAD y SYDP, consulte [directrices para asociaciones de archivos y programas predeterminados](appguide-fa-defpro.md), y [establecer el acceso a programas y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md).

 

## <a name="finding-an-application-executable"></a>Buscar un archivo ejecutable de aplicación

Cuando se llama a la función [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con el nombre de un archivo ejecutable en su parámetro *lpFile* , hay varios lugares en los que la función busca el archivo. Se recomienda registrar la aplicación en la subclave del registro de rutas de acceso de la **aplicación** . Al hacerlo, se evita la necesidad de que las aplicaciones modifiquen la variable de entorno de la ruta de acceso del sistema.

El archivo se busca en las siguientes ubicaciones:

-   El directorio de trabajo actual.
-   Solo el directorio de **Windows** (no se busca ningún subdirectorio).
-   Directorio **\\ system32 de Windows** .
-   Directorios enumerados en la variable de entorno PATH.
-   Recomendado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**

## <a name="registering-applications"></a>Registro de aplicaciones

Las subclaves del registro de **aplicaciones** y rutas de acceso de la **aplicación** se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones. La subclave de rutas de acceso de la **aplicación** es la ubicación preferida.

### <a name="using-the-app-paths-subkey"></a>Usar la subclave de rutas de acceso de la aplicación

En Windows 7 y versiones posteriores, se recomienda encarecidamente instalar aplicaciones por usuario en lugar de por equipo. Una aplicación que se instala para por usuario puede registrarse en **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**. Una aplicación que se instala para todos los usuarios del equipo se puede registrar en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**.

Las entradas que se encuentran en rutas de acceso de la **aplicación** se usan principalmente para los siguientes fines:

-   Para asignar el nombre del archivo ejecutable de una aplicación a la ruta de acceso completa del archivo.
-   Para dejar pendiente la información en la variable de entorno PATH por aplicación y por proceso.

Si el nombre de una subclave de rutas de acceso de la **aplicación** coincide con el nombre de archivo, el shell realiza dos acciones:

-   La entrada (predeterminada) se usa como ruta de acceso completa del archivo.
-   La entrada de la ruta de acceso de la subclave se antepone a la variable de entorno PATH de ese proceso. Si no es necesario, se puede omitir el valor de la ruta de acceso.

Los posibles problemas que se deben tener en cuenta son:

-   El shell limita la longitud de una línea de comandos a la ruta de acceso máxima de \_ \* 2 caracteres. Si hay muchos archivos enumerados como entradas del registro o sus rutas de acceso son largas, los nombres de archivo que se encuentran más adelante en la lista podrían perderse mientras se trunca la línea de comandos.
-   Algunas aplicaciones no aceptan varios nombres de archivo en una línea de comandos.
-   Algunas aplicaciones que aceptan varios nombres de archivo no reconocen el formato en el que el Shell las proporciona. El Shell proporciona la lista de parámetros como una cadena entrecomillada, pero algunas aplicaciones pueden requerir cadenas sin comillas.
-   No todos los elementos que se pueden arrastrar son parte del sistema de archivos; por ejemplo, impresoras. Estos elementos no tienen una ruta de acceso de Win32 estándar, por lo que no hay ninguna manera de proporcionar un valor de *lpParameters* significativo a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

El uso de la entrada DropTarget evita estos posibles problemas al proporcionar acceso a todos los formatos del portapapeles, incluido [CFSTR \_ SHELLIDLIST](clipboard.md) (para las listas de archivos largos) y [CFSTR \_ FILECONTENTS](clipboard.md) (para los objetos que no son del sistema de archivos).

**Para registrar y controlar el comportamiento de las aplicaciones con la subclave de rutas de acceso de la aplicación**:

1.  Agregue una subclave con el mismo nombre que el archivo ejecutable a la subclave de rutas de acceso de la **aplicación** , tal como se muestra en la siguiente entrada del registro.

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  Vea la tabla siguiente para obtener detalles de las entradas de la subclave **paths de aplicación** . 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Entrada del Registro</th>
    <th>Detalles</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>(Es el valor predeterminado).</td>
    <td>Es la ruta de acceso completa a la aplicación. El nombre de la aplicación proporcionado en la entrada (valor predeterminado) se puede indicar con o sin la extensión. exe. Si es necesario, la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> agrega la extensión al buscar la subclave de rutas de acceso de la <strong>aplicación</strong> . La entrada es del tipo de <strong>REG_SZ</strong> .</td>
    </tr>
    <tr class="even">
    <td>DontUseDesktopChangeRouter</td>
    <td>Es obligatorio para que las aplicaciones del depurador eviten los interbloqueos del cuadro de diálogo de archivo al depurar el proceso del explorador de Windows. Sin embargo, el establecimiento de la entrada DontUseDesktopChangeRouter produce un control ligeramente menos eficaz de las notificaciones de cambios. La entrada es del tipo <strong>REG_DWORD</strong> y el valor es 0x1.</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>Es un identificador de clase (CLSID). La entrada DropTarget contiene el CLSID de un objeto (normalmente un servidor local en lugar de un servidor en proceso) que implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>. De forma predeterminada, cuando el destino de colocación es un archivo ejecutable y no se proporciona ningún valor de DropTarget, el shell convierte la lista de archivos colocados en un parámetro de línea de comandos y lo pasa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> a través de <em>lpParameters</em>.</td>
    </tr>
    <tr class="even">
    <td>Ruta</td>
    <td>Proporciona una cadena (en forma de lista de directorios separados por punto y coma) para anexar a la variable de entorno PATH cuando se inicia una aplicación mediante una llamada a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>. Es la ruta de acceso completa al archivo. exe. Es de <strong>REG_SZ</strong>. En <strong>Windows 7 y versiones posteriores</strong>, el tipo se puede <strong>REG_EXPAND_SZ</strong>y suele ser <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.
    <blockquote>
    [!Note]<br />
Además de las entradas (default), path y DropTarget reconocidas por el Shell, una aplicación también puede agregar valores personalizados a la subclave de las <strong>rutas</strong> de acceso de la aplicación de su archivo ejecutable. Se recomienda a los desarrolladores de aplicaciones que usen la subclave <strong>App paths</strong> para proporcionar una ruta de acceso específica de la aplicación en lugar de realizar adiciones a la ruta de acceso global del sistema.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>Crea una cadena que contiene los esquemas de protocolo de dirección URL para una clave determinada. Puede contener varios valores del registro para indicar qué esquemas se admiten. Esta cadena sigue el formato de <strong>scheme1: scheme2</strong>. Si esta lista no está vacía, se agregará <strong>File:</strong> a la cadena. Este protocolo se admite implícitamente cuando se define <em>SupportedProtocols</em> . <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>Indica que la aplicación puede aceptar una dirección URL (en lugar de un nombre de archivo) en la línea de comandos. Las aplicaciones que pueden abrir documentos directamente desde Internet, como los exploradores Web y los reproductores multimedia, deben establecer esta entrada. <br/> Cuando la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> inicia una aplicación y no se establece el valor UseUrl = 1, <strong>ShellExecuteEx</strong> descarga el documento en un archivo local e invoca el controlador en la copia local.<br/> Por ejemplo, si la aplicación tiene este conjunto de entrada y un usuario hace clic con el botón secundario en un archivo almacenado en un servidor Web, el verbo abierto estará disponible. Si no es así, el usuario tendrá que descargar el archivo y abrir la copia local. <br/> La entrada UseUrl es de <strong>REG_DWORD</strong> tipo y el valor es 0x1.<br/> En Windows Vista y versiones anteriores, esta entrada indicaba que la dirección URL se debe pasar a la aplicación junto con un nombre de archivo local, cuando se llama a través de ShellExecuteEx. En Windows 7, indica que la aplicación puede comprender cualquier dirección URL http o https que se le pase, sin tener que proporcionar también el nombre del archivo de caché. Esta clave del registro está asociada a la clave <em>SupportedProtocols</em> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>Usar la subclave Applications

A través de la inclusión de entradas del registro en la subclave **HKEY \_ classes \_ root** \\ **Applications** \\ *ApplicationName.exe* , las aplicaciones pueden proporcionar la información específica de la aplicación que se muestra en la tabla siguiente.



| Entrada del Registro                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verbo de Shell \\                      | Proporciona el método de verbo para llamar a la aplicación desde OpenWith. Sin una definición de verbo especificada aquí, el sistema supone que la aplicación admite [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)y pasa el nombre de archivo en la línea de comandos. Esta funcionalidad se aplica a todos los métodos de verbo, incluidos DropTarget, ExecuteCommand y Intercambio dinámico de datos (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Permite a una aplicación proporcionar un icono específico para representar la aplicación en lugar del primer icono almacenado en el archivo. exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Proporciona una manera de obtener un nombre traducible para mostrarlo en una aplicación, en lugar de solo la información de versión que aparece, que puede no ser localizable. La consulta de asociación [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) Lee este valor de entrada del registro y revierte a usar el nombre de FileDescription en la información de versión. Si falta ese nombre, la consulta de asociación tiene como valor predeterminado el nombre para mostrar del archivo. Las aplicaciones deben usar **ASSOCSTR \_ FRIENDLYAPPNAME** para recuperar esta información con el fin de obtener el comportamiento correcto.                                                                                                                                                                        |
| SupportedTypes                   | Enumera los tipos de archivo que admite la aplicación. Esto permite que la aplicación se muestre en el menú en cascada del cuadro de diálogo **abrir con** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indica que no se ha especificado ninguna aplicación para abrir este tipo de archivo. Tenga en cuenta que si se ha establecido una subclave OpenWithProgIDs para una aplicación por tipo de archivo, y la propia subclave ProgID no tiene también una entrada NoOpenWith, esa aplicación aparecerá en la lista de aplicaciones recomendadas o disponibles incluso si se ha especificado la entrada NoOpenWith. Para obtener más información, vea cómo [incluir una aplicación en el cuadro de diálogo Abrir con](how-to-include-an-application-on-the-open-with-dialog-box.md) y [Cómo excluir una aplicación del cuadro de diálogo Abrir con](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indica que el proceso es un proceso de host, como Rundll32.exe o Dllhost.exe, y no debe tenerse en cuenta para el anclaje o la inclusión del menú **Inicio** en la lista de usados con mayor frecuencia (MFU). Cuando se inicia con un acceso directo que contiene una lista de argumentos que no son NULL o un [identificador de modelo de usuario de aplicación explícito (AppUserModelIDs)](appids.md), el proceso se puede anclar (como ese método abreviado). Estos métodos abreviados son candidatos para su inclusión en la lista de MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indica que el archivo ejecutable de la aplicación y los accesos directos deben excluirse del menú **Inicio** y de anclarse o incluirse en la lista de MFU. Esta entrada se usa normalmente para excluir las herramientas del sistema, los instaladores y los desinstaladores, y los archivos Léame.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Hace que la barra de tareas Use el icono predeterminado de este archivo ejecutable si no hay ningún acceso directo anclado para esta aplicación y en lugar del icono de la ventana que se encontró por primera vez.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Especifica el icono que se usa para invalidar el icono de la barra de tareas. El icono de ventana se usa normalmente para la barra de tareas. La configuración de la entrada TaskbarGroupIcon hace que el sistema use en su lugar el icono del archivo. exe para la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos de registros de aplicación a través de la subclave de aplicaciones **\_ \_ raíz de las clases HKEY** \\  \\ *ApplicationName.exe* . Todos los valores de entrada del registro son del tipo **reg \_ SZ** , con la excepción de **DefaultIcon** , que es de tipo **reg \_ Expand \_** .

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>Registrar verbos y otra información de Asociación de archivos

Las subclaves registradas en **\_ las clases HKEY \_ raíz** \\ **SystemFileAssociations** permiten al shell definir el comportamiento predeterminado de los atributos de los tipos de archivo y habilitar las asociaciones de archivos compartidos. Cuando los usuarios cambian la aplicación predeterminada para un tipo de archivo, el ProgID de la nueva aplicación predeterminada tiene prioridad en proporcionar verbos y otra información de asociación. Esta prioridad se debe a que es la primera entrada de la matriz de asociaciones. Si se cambia el programa predeterminado, la información del ProgID anterior ya no está disponible.

Para tratar de forma proactiva las consecuencias de un cambio en los programas predeterminados, puede usar **\_ las clases HKEY \_ raíz** \\ **SystemFileAssociations** para registrar verbos y otra información de asociación. Debido a su ubicación después del identificador de programa (ProgID) de la matriz de asociaciones, estos registros tienen una prioridad más baja. Estos SystemFileAssociationsregistrations son estables incluso cuando los usuarios cambian los programas predeterminados y proporcionan una ubicación para registrar verbos secundarios que siempre estarán disponibles para un tipo de archivo determinado. Para obtener un ejemplo del registro, vea [registrar un tipo percibido](#registering-a-perceived-type) más adelante en este tema.

En el ejemplo del Registro siguiente se muestra lo que ocurre cuando el usuario ejecuta el elemento **programas predeterminados** en el panel de control para cambiar el valor predeterminado de los archivos. mp3 a App2ProgID. Después de cambiar el valor predeterminado, Verb1 ya no está disponible y Verb2 se convierte en el valor predeterminado.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>Registrar un tipo percibido

Los valores del registro para los tipos percibidos se definen como subclaves de la subclave del registro SystemFileAssociations de **\_ las clases HKEY \_ raíz** \\  . Por ejemplo, el **texto** de tipo percibido se registra de la siguiente manera:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

El tipo percibido de un tipo de archivo se indica incluyendo un valor PerceivedType en la subclave del tipo de archivo. El valor PerceivedType se establece en el nombre del tipo percibido registrado en la subclave del registro SystemFileAssociations de **\_ las clases \_ HKEY** \\  , tal como se muestra en el ejemplo del registro anterior. Para declarar los archivos. cpp como de tipo "texto" percibido, por ejemplo, agregue la siguiente entrada del registro:

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

