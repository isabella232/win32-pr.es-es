---
description: En este tema se describe cómo las aplicaciones pueden exponer información sobre sí mismas necesarias para habilitar determinados escenarios.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registro de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac1c72614ce3241cbac6b880b0d9f5f84f9fbf85c8ee022d83574df6d86e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224947"
---
# <a name="application-registration"></a>Registro de la aplicación

En este tema se describe cómo las aplicaciones pueden exponer información sobre sí mismas necesarias para habilitar determinados escenarios. Esto incluye la información necesaria para localizar la aplicación, los verbos que admite la aplicación y los tipos de archivos que una aplicación puede controlar.

Este tema se organiza de la siguiente manera:

-   [Buscar un ejecutable de aplicación](#finding-an-application-executable)
-   [Registro de aplicaciones](#registering-applications)
    -   [Uso de la subclave Rutas de acceso de la aplicación](#using-the-app-paths-subkey)
    -   [Uso de la subclave Aplicaciones](#using-the-applications-subkey)
-   [Registrar verbos y otra información de asociación de archivos](#registering-verbs-and-other-file-association-information)
-   [Registrar un tipo percibido](#registering-a-perceived-type)
-   [Temas relacionados](#related-topics)

> [!Note]  
> Las aplicaciones también se pueden registrar en las aplicaciones del panel de control Set Program Access and Computer Defaults (SPAD) y Set Your Default Programs (SYDP). Para obtener información sobre el registro de aplicaciones SPAD y SYDP, vea [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md)y Set Program Access and Computer [Defaults (SPAD).](cpl-setprogramaccess.md)

 

## <a name="finding-an-application-executable"></a>Buscar un ejecutable de aplicación

Cuando se llama a la función [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con el nombre de un archivo ejecutable en su parámetro *lpFile,* hay varios lugares donde la función busca el archivo. Se recomienda registrar la aplicación en la subclave del Registro **rutas** de acceso de la aplicación. Esto evita la necesidad de que las aplicaciones modifiquen la variable de entorno PATH del sistema.

El archivo se busca en las siguientes ubicaciones:

-   El directorio de trabajo actual.
-   Solo **Windows** directorio (no se busca ningún subdirectorio).
-   Directorio **Windows \\ System32.**
-   Directorios enumerados en la variable de entorno PATH.
-   Recomendado: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **Rutas de acceso de la aplicación** \\ **CurrentVersion**

## <a name="registering-applications"></a>Registro de aplicaciones

Las **subclaves del** Registro Rutas de acceso de la aplicación y Aplicaciones se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones.  La **subclave Rutas** de acceso de la aplicación es la ubicación preferida.

### <a name="using-the-app-paths-subkey"></a>Uso de la subclave Rutas de acceso de la aplicación

En Windows 7 y versiones posteriores, se recomienda encarecidamente instalar aplicaciones por usuario en lugar de por máquina. Una aplicación que se instala para por usuario se puede registrar en **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Rutas de acceso de la** aplicación \\ **CurrentVersion**. Una aplicación que se instala para todos los usuarios del equipo se puede registrar en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **rutas de acceso de la** aplicación \\ **CurrentVersion**.

Las entradas que se encuentran en **Rutas de acceso de** la aplicación se usan principalmente con los siguientes fines:

-   Para asignar el nombre de archivo ejecutable de una aplicación a la ruta de acceso completa de ese archivo.
-   Para obtener información previa a la variable de entorno PATH por aplicación y por proceso.

Si el nombre de una subclave de **rutas** de acceso de aplicación coincide con el nombre de archivo, shell realiza dos acciones:

-   La entrada (valor predeterminado) se usa como ruta de acceso completa del archivo.
-   La entrada Path de esa subclave se ha pendido previamente en la variable de entorno PATH de ese proceso. Si no es necesario, se puede omitir el valor path.

Entre los posibles problemas que se deben tener en cuenta se incluyen:

-   El shell limita la longitud de una línea de comandos a MAX \_ PATH \* 2 caracteres. Si hay muchos archivos enumerados como entradas del Registro o sus rutas de acceso son largas, los nombres de archivo más adelante en la lista podrían perderse a medida que se trunca la línea de comandos.
-   Algunas aplicaciones no aceptan varios nombres de archivo en una línea de comandos.
-   Algunas aplicaciones que aceptan varios nombres de archivo no reconocen el formato en el que el Shell los proporciona. Shell proporciona la lista de parámetros como una cadena entre comillas, pero algunas aplicaciones pueden requerir cadenas sin comillas.
-   No todos los elementos que se pueden arrastrar forman parte del sistema de archivos; por ejemplo, impresoras. Estos elementos no tienen una ruta de acceso estándar de Win32, por lo que no hay ninguna manera de proporcionar un valor *lpParameters* significativo a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

El uso de la entrada DropTarget evita estos posibles problemas al proporcionar acceso a todos los formatos del Portapapeles, [incluidos CFSTR \_ SHELLIDLIST](clipboard.md) (para listas de archivos largas) y [CFSTR \_ FILECONTENTS](clipboard.md) (para objetos que no son del sistema de archivos).

**Para registrar y controlar el comportamiento de las aplicaciones con la subclave Rutas de acceso de la aplicación**:

1.  Agregue una subclave con el mismo nombre que el archivo ejecutable a la subclave **Rutas** de acceso de la aplicación, como se muestra en la siguiente entrada del Registro.

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

2.  Consulte la tabla siguiente para obtener más información sobre las entradas de la subclave **Rutas** de acceso de la aplicación. 

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
    <td>Es la ruta de acceso completa a la aplicación. El nombre de la aplicación proporcionado en la entrada (valor predeterminado) se puede indicar con o sin su .exe extensión. Si es necesario, la <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>función ShellExecuteEx</strong></a> agrega la extensión al buscar la subclave <strong>Rutas de acceso de</strong> la aplicación. La entrada es del <strong>tipo REG_SZ</strong> entrada.</td>
    </tr>
    <tr class="even">
    <td>DontUseDesktopChangeRouter</td>
    <td>Es obligatorio para que las aplicaciones del depurador eviten interbloqueos en el cuadro de diálogo de archivos al depurar el Windows Explorer. Sin embargo, al establecer la entrada DontUseDesktopChangeRouter se produce un control ligeramente menos eficaz de las notificaciones de cambio. La entrada es del <strong>tipo REG_DWORD</strong> y el valor es 0x1.</td>
    </tr>
    <tr class="odd">
    <td>DropTarget</td>
    <td>Es un identificador de clase (CLSID). La entrada DropTarget contiene el CLSID de un objeto (normalmente un servidor local en lugar de un servidor en proceso) que implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>. De forma predeterminada, cuando el destino de colocación es un archivo ejecutable y no se proporciona ningún valor DropTarget, el Shell convierte la lista de archivos eliminados en un parámetro de línea de comandos y lo pasa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> a <em>través de lpParameters</em>.</td>
    </tr>
    <tr class="even">
    <td>Ruta de acceso</td>
    <td>Proporciona una cadena (en forma de una lista de directorios separados por punto y coma) para anexar a la variable de entorno PATH cuando se inicia una aplicación mediante una llamada a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>. Es la ruta de acceso completa al .exe. Es de <strong>REG_SZ</strong>. En <strong>Windows 7 y</strong>versiones posteriores, el tipo se puede REG_EXPAND_SZ y se REG_EXPAND_SZ %ProgramFiles%. <strong></strong> <strong></strong>
    <blockquote>
    [!Note]<br />
Además de las entradas (Valor predeterminado), Ruta de acceso y DropTarget reconocidas por el Shell, una aplicación también puede agregar valores personalizados a la <strong>subclave</strong> Rutas de acceso de aplicación de su archivo ejecutable. Animamos a los desarrolladores de aplicaciones a usar la subclave <strong>Rutas</strong> de acceso de la aplicación para proporcionar una ruta de acceso específica de la aplicación en lugar de realizar adiciones a la ruta de acceso del sistema global.
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>SupportedProtocols</td>
    <td>Crea una cadena que contiene los esquemas de protocolo de dirección URL para una clave determinada. Puede contener varios valores del Registro para indicar qué esquemas se admiten. Esta cadena sigue el formato de <strong>scheme1:scheme2</strong>. Si esta lista no está vacía, se agregará <strong>file:</strong> a la cadena. Este protocolo se admite implícitamente cuando <em>se define SupportedProtocols.</em> <br/></td>
    </tr>
    <tr class="even">
    <td>UseUrl</td>
    <td>Indica que la aplicación puede aceptar una dirección URL (en lugar de un nombre de archivo) en la línea de comandos. Las aplicaciones que pueden abrir documentos directamente desde Internet, como exploradores web y reproductores multimedia, deben establecer esta entrada. <br/> Cuando la <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>función ShellExecuteEx</strong></a> inicia una aplicación y no se establece el valor UseUrl=1, <strong>ShellExecuteEx</strong> descarga el documento en un archivo local e invoca el controlador en la copia local.<br/> Por ejemplo, si la aplicación tiene este conjunto de entradas y un usuario hace clic con el botón derecho en un archivo almacenado en un servidor web, el verbo Abrir estará disponible. Si no es así, el usuario tendrá que descargar el archivo y abrir la copia local. <br/> La entrada UseUrl es de <strong>REG_DWORD</strong> y el valor es 0x1.<br/> En Windows Vista y versiones anteriores, esta entrada indicaba que la dirección URL se debe pasar a la aplicación junto con un nombre de archivo local, cuando se llama a través de ShellExecuteEx. En Windows 7, indica que la aplicación puede comprender cualquier dirección URL http o https que se le pase, sin tener que proporcionar también el nombre del archivo de caché. Esta clave del Registro está asociada a <em>la clave SupportedProtocols.</em><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a>Uso de la subclave Aplicaciones

Mediante la inclusión de entradas del Registro en la subclave **HKEY \_ CLASSES \_ ROOT** \\ **Applications** \\ *ApplicationName.exe,* las aplicaciones pueden proporcionar la información específica de la aplicación que se muestra en la tabla siguiente.



| Entrada del Registro                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verbo \\ shell                      | Proporciona el método verbo para llamar a la aplicación desde OpenWith. Sin una definición de verbo especificada aquí, el sistema asume que la aplicación admite [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)y pasa el nombre de archivo en la línea de comandos. Esta funcionalidad se aplica a todos los métodos de verbo, incluidos DropTarget, ExecuteCommand y datos dinámicos Exchange (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Permite que una aplicación proporcione un icono específico para representar la aplicación en lugar del primer icono almacenado en .exe archivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Proporciona una manera de obtener un nombre localizable para mostrar para una aplicación en lugar de solo la información de versión que aparece, que puede no ser localizable. La consulta de [**asociación ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) lee este valor de entrada del Registro y vuelve a usar el nombre FileDescription en la información de versión. Si falta ese nombre, la consulta de asociación tiene como valor predeterminado el nombre para mostrar del archivo. Las aplicaciones deben **usar ASSOCSTR \_ FRIENDLYAPPNAME para** recuperar esta información con el fin de obtener el comportamiento adecuado.                                                                                                                                                                        |
| SupportedTypes                   | Enumera los tipos de archivo que admite la aplicación. Esto permite que la aplicación aparezca en el menú en cascada del **Abrir con** diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indica que no se especifica ninguna aplicación para abrir este tipo de archivo. Tenga en cuenta que si se ha establecido una subclave OpenWithProgIDs para una aplicación por tipo de archivo y la propia subclave ProgID no tiene también una entrada NoOpenWith, esa aplicación aparecerá en la lista de aplicaciones recomendadas o disponibles incluso si ha especificado la entrada NoOpenWith. Para obtener más información, vea [How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) (Cómo incluir una aplicación en el cuadro de diálogo Abrir con) y How to exclude an Application from the Abrir con Dialog [Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indica que el proceso es un proceso host, como Rundll32.exe o Dllhost.exe, y  no debe considerarse para la anclar o inclusión del menú Inicio en la lista Más usados (MFU). Cuando se inicia con un acceso directo que contiene una lista de argumentos no NULL o un id. de modelo de usuario de aplicación [explícito (AppUserModelID),](appids.md)el proceso se puede anclar (como ese acceso directo). Estos accesos directos son candidatos para su inclusión en la lista de MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indica que el archivo ejecutable y los accesos directos de la aplicación deben excluirse del menú Inicio y de anclar o incluir en la lista MFU.  Esta entrada se usa normalmente para excluir herramientas del sistema, instaladores, desinstaladores y archivos Léame.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Hace que la barra de tareas use el icono predeterminado de este ejecutable si no hay ningún acceso directo anclable para esta aplicación y en lugar del icono de la ventana que se encontró por primera vez.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Especifica el icono usado para invalidar el icono de la barra de tareas. El icono de ventana se usa normalmente para la barra de tareas. Al establecer la entrada TaskbarGroupIcon, el sistema usará el icono de la .exe para la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Ejemplos

A continuación se muestran algunos ejemplos de registros de aplicaciones a través de las aplicaciones raíz **ApplicationName.exeHKEY \_ \_ CLASSES.** \\  \\ ** Todos los valores de entrada del Registro son **de tipo REG \_ SZ,** a excepción de **DefaultIcon,** que es del **tipo REG EXPAND \_ \_ SZ.**

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

## <a name="registering-verbs-and-other-file-association-information"></a>Registrar verbos y otra información de asociación de archivos

Las subclaves registradas en **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** permiten al shell definir el comportamiento predeterminado de los atributos para los tipos de archivo y habilitar las asociaciones de archivo compartido. Cuando los usuarios cambian la aplicación predeterminada para un tipo de archivo, el ProgID de la nueva aplicación predeterminada tiene prioridad en proporcionar verbos y otra información de asociación. Esta prioridad se debe a que es la primera entrada de la matriz de asociación. Si se cambia el programa predeterminado, la información del ProgID anterior ya no está disponible.

Para tratar de forma proactiva las consecuencias de un cambio en los programas predeterminados, puede usar **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations** para registrar verbos y otra información de asociación. Debido a su ubicación después del ProgID en la matriz de asociación, estos registros son de menor prioridad. Estas SystemFileAssociationsregistrations son estables incluso cuando los usuarios cambian los programas predeterminados y proporcionan una ubicación para registrar verbos secundarios que siempre estarán disponibles para un tipo de archivo determinado. Para obtener un ejemplo del Registro, [vea Registrar un tipo percibido](#registering-a-perceived-type) más adelante en este tema.

En el ejemplo del Registro siguiente  se muestra lo que sucede cuando el usuario ejecuta el elemento Programas predeterminados en Panel de control para cambiar el valor predeterminado de los archivos .mp3 a App2ProgID. Después de cambiar el valor predeterminado, Verb1 ya no está disponible y Verb2 se convierte en el valor predeterminado.

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

Los valores del Registro para los tipos percibidos se definen como subclaves de la subclave del Registro **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations.** Por ejemplo, el texto de tipo **percibido** se registra de la siguiente manera:

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

El tipo percibido de un tipo de archivo se indica mediante la inclusión de un valor PerceivedType en la subclave del tipo de archivo. El valor PerceivedType se establece en el nombre del tipo percibido registrado en la subclave del Registro **HKEY \_ CLASSES \_ ROOT** \\ **SystemFileAssociations,** como se muestra en el ejemplo anterior del Registro. Para declarar archivos .cpp como de tipo percibido "text", por ejemplo, agregue la siguiente entrada del Registro:

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivo](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo o tipo de archivo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipos de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores mediante programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

