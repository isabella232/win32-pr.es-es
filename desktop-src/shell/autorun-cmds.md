---
description: Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun. inf. Una entrada consta de una clave y un valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas Autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275248"
---
# <a name="autoruninf-entries"></a>Entradas Autorun. inf

Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun. inf. Una entrada consta de una clave y un valor.

-   [\[Claves de ejecución automática \]](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [icono](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [ShellExecute](#shellexecute)
    -   [interfaz](#autoruninf-entries)
    -   [verbo de Shell \\](#shellverb)
-   [\[Claves de contenido \]](#content-keys)
-   [\[Claves de ExclusiveContentPaths \]](#exclusivecontentpaths-keys)
-   [\[Claves de IgnoreContentPaths \]](#ignorecontentpaths-keys)
-   [\[Claves de DeviceInstall \]](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[Claves de ejecución automática \]

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [icono](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [ShellExecute](#shellexecute)
-   [interfaz](#autoruninf-entries)
-   [verbo de Shell \\](#shellverb)

### <a name="action"></a>action

La entrada de **acción** especifica el texto que se utiliza en el cuadro de diálogo reproducción automática del controlador que representa el programa especificado en la entrada [Open](#parameters) o [ShellExecute](#shellexecute) del archivo Autorun. inf del medio. El valor se puede expresar como texto o como un recurso almacenado en un archivo binario.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parámetros

-   *ActionText*

    Texto que se usa en el cuadro de diálogo reproducción automática del controlador que representa el programa especificado en la entrada [Open](#parameters) o [ShellExecute](#shellexecute) del archivo Autorun. inf del medio.

-   *filepath*

    Cadena que contiene la ruta de acceso completa del directorio que contiene el archivo binario que contiene la cadena. Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.

-   *filename*

    Cadena que contiene el nombre del archivo binario.

-   *Identificador*

    IDENTIFICADOR de la cadena dentro del archivo binario.

### <a name="remarks"></a>Observaciones

La clave de **acción** solo se utiliza en Windows XP Service Pack 2 (SP2) o posterior. Solo se admite para las unidades de tipo unidad \_ extraíble y unidad \_ fija. En el caso de la unidad \_ extraíble, se requiere la clave de **acción** . Se omite un comando de **acción** en el archivo Autorun. inf de un CD de audio o un DVD de película, y estos medios continúan comportados como en Windows XP Service Pack 1 (SP1) y versiones anteriores.

La cadena mostrada en el cuadro de diálogo reproducción automática se construye combinando el texto especificado en la entrada de **acción** con el nombre de texto codificado de forma rígida del proveedor, proporcionado por el shell. Se muestra el [icono](#parameters) junto a él. Esta entrada siempre aparece como la primera opción en el cuadro de diálogo reproducción automática y está seleccionada de forma predeterminada. Si el usuario acepta la opción, se inicia la aplicación especificada por la entrada [Open](#parameters) o [ShellExecute](#shellexecute) en el archivo Autorun. inf del medio. La opción **siempre la acción seleccionada** no está disponible en esta situación.

Las claves de [acción](#parameters) y [icono](#parameters) definen conjuntamente la representación de la aplicación que el usuario final verá en el cuadro de diálogo reproducción automática. Deberían estar compuestas de forma que los usuarios puedan identificarlas fácilmente. Deben indicar la aplicación que se va a ejecutar, la compañía que la creó y cualquier personalización de marca asociada.

Por compatibilidad con versiones anteriores, la entrada de **acción** es opcional para los dispositivos de tipo Drive \_ fixed. Para este tipo, se usa una entrada predeterminada en el cuadro de diálogo reproducción automática si no hay ninguna entrada de **acción** en el archivo Autorun. inf.

La entrada de **acción** es obligatoria para los dispositivos de tipo unidad \_ extraíbles, que hasta ahora no tienen compatibilidad con Autorun. inf. Si no hay ninguna entrada de **acción** , se muestra el cuadro de diálogo reproducción automática, pero sin ninguna opción para iniciar el contenido adicional.

### <a name="customevent"></a>CustomEvent

La entrada **CustomEvent** especifica un evento de contenido personalizado de reproducción automática.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parámetros

-   *CustomEventName*

    Cadena de texto que contiene el nombre del evento de contenido de reproducción automática. El nombre no debe tener más de 100 caracteres alfanuméricos.

### <a name="remarks"></a>Observaciones

Puede incluir un nombre de evento personalizado en el archivo Autorun. inf de un volumen. Cuando la reproducción automática solicita al usuario una aplicación para usarla con el volumen, solo muestra las aplicaciones que se han registrado para el nombre de evento personalizado especificado. Para obtener información sobre cómo registrar una aplicación como un controlador para el evento personalizado de contenido de reproducción automática, consulte [Inicio automático con reproducción automática](/previous-versions/windows/apps/hh452731(v=win.10)) o [registro de un controlador de eventos](how-to-register-an-event-handler.md).

En el ejemplo siguiente se especifica el valor "MyContentOnArrival" como nuevo evento de contenido de reproducción automática.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

La entrada **Icon** especifica un icono que representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parámetros

-   *IconFileName*

    Nombre de un archivo. ico,. bmp,. exe o. dll que contiene la información del icono. Si un archivo contiene más de un icono, también debe especificar un índice basado en cero del icono.

### <a name="remarks"></a>Observaciones

El icono, junto con la etiqueta, representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows. Por ejemplo, en el explorador de Windows, la unidad está representada por este icono en lugar del icono de la unidad estándar. El archivo del icono debe estar en el mismo directorio que el archivo especificado por el comando [abrir](#parameters) .

En el ejemplo siguiente se especifica el segundo icono del archivo de MyProg.exe.


```
icon=MyProg.exe,1
```



### <a name="label"></a>etiqueta

La entrada **etiqueta** especifica una etiqueta de texto que representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.


```
label=LabelText
```



### <a name="parameters"></a>Parámetros

-   *LabelText*

    Cadena de texto que contiene la etiqueta. Puede contener espacios y no debe tener más de 32 caracteres.

> [!Note]  
> Es posible colocar un valor en el parámetro **LabelText** que supere los 32 caracteres y no reciba ningún mensaje de error. Sin embargo, el sistema solo muestra los primeros 32 caracteres. Los caracteres situados después del 32 º se truncan y no se muestran. Por ejemplo, si el **LabelText** es el siguiente: etiqueta = "este CD está diseñado para ser el CD de música Ultimate". se mostrará lo siguiente: "este CD está diseñado para ser el UL".

 

### <a name="remarks"></a>Observaciones

La etiqueta, junto con un icono, representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.

En el ejemplo siguiente se especifica el valor "mi etiqueta de unidad" como etiqueta de la unidad.


```
label=My Drive Label
```



### <a name="open"></a>abrir

La entrada **Open** especifica la ruta de acceso y el nombre de archivo de la aplicación que se inicia automáticamente cuando un usuario inserta un disco en la unidad.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parámetros

-   *exefile*

    Ruta de acceso completa de un archivo ejecutable que se ejecuta cuando se inserta el CD. Si solo se especifica un nombre de archivo, debe estar en el directorio raíz de la unidad. Para buscar el archivo en un subdirectorio, debe especificar una ruta de acceso. También puede incluir uno o varios parámetros de la línea de comandos para pasarlos a la aplicación de inicio.

### <a name="useautoplay"></a>UseAutoPlay

En Windows XP, la entrada **UseAutoPlay** especifica que se debe usar la reproducción automática en lugar de la ejecución automática.

En Windows Vista y versiones posteriores, esta entrada hace que se eliminen todas las acciones especificadas para la ejecución automática (mediante las entradas **Open** o **ShellExecute** ) en el cuadro de diálogo reproducción automática. Esta entrada no tiene ningún efecto en las versiones de Windows anteriores a Windows XP.

En Windows 8 y versiones posteriores, si se especifica un valor de 0, se deshabilitará la reproducción automática para este dispositivo.

### <a name="parameters"></a>Parámetros

Para usar esta opción, agregue una entrada para **UseAutoPlay** al archivo Autorun. inf y establezca la entrada igual a 1. No se admite ningún otro valor en versiones de Windows anteriores a Windows 8.

En Windows 8 y versiones posteriores, especifique un valor de 0 para deshabilitar la reproducción automática para este dispositivo.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Observaciones

Actualmente, **UseAutoPlay** solo es aplicable en Windows XP o posterior y solo en una unidad que [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina como de tipo **unidad \_ CDROM**.

Cuando se utiliza **UseAutoPlay** , cualquier acción especificada por las entradas **Open** o **ShellExecute** en Autorun. inf se omite en Windows XP y se omite en el cuadro de diálogo reproducción automática en Windows Vista.

La ejecución automática se usa normalmente para ejecutar automáticamente o cargar algo incluido en el medio insertado, mientras que la reproducción automática presenta un cuadro de diálogo que incluye una lista de las acciones pertinentes que se pueden realizar y permite al usuario elegir qué acción debe realizar. Para obtener más información acerca de la diferencia entre la ejecución automática y la reproducción automática, consulte [crear una aplicación de CD-ROM habilitada para Autorun](autoplay.md) y [usar y configurar la reproducción automática](autoplay2k-using.md), respectivamente.

### <a name="usage-example"></a>Ejemplo de uso

Un CD contiene tres archivos: Autorun. inf, Readme.txt y Music. WMA. Dependiendo de la versión de Windows en uso y de las opciones especificadas en Autorun. inf, el CD se puede controlar mediante la ejecución automática o la reproducción automática cuando se inserte (suponiendo que la ejecución automática o la reproducción automática esté habilitada para la unidad en la que se inserta el CD).

En primer lugar, considere un archivo Autorun. inf con el siguiente contenido, teniendo en cuenta que no se especifica **UseAutoPlay = 1** :


```
[AutoRun]
shellexecute="Readme.txt"
```



La acción realizada por el shell al insertar este CD depende de la versión de Windows en uso:

-   En Windows XP o versiones anteriores, este CD se administra mediante la ejecución automática cuando se inserta. En este caso, se lee la entrada **ShellExecute** y el shell invoca el controlador de archivos asociado a los archivos. txt. Normalmente, se abriría Readme.txt en el Bloc de notas.
-   En Windows Vista, la presencia de un archivo Autorun. inf con una entrada **ShellExecute** hace que los medios se identifiquen como tipo de reproducción automática "Software and Games". En este caso, se muestra al usuario un cuadro de diálogo de reproducción automática que incluye la acción especificada por la entrada **ShellExecute** (presentada como "cargar Readme.txt" en el cuadro de diálogo), junto con las acciones predeterminadas asociadas a los medios de tipo "Software and Games".

Para indicar que se debe usar la reproducción automática en lugar de la ejecución automática en Windows XP, y que la acción especificada por la entrada ShellExecute de ejecución se debe suprimir en el cuadro de diálogo reproducción automática en Windows Vista, inserte **UseAutoPlay** en el archivo Autorun. inf de la manera siguiente:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



Una vez más, la acción realizada por el shell al insertar este CD depende de la versión de Windows en uso.

-   En las versiones de Windows anteriores a Windows XP, se sigue usando la ejecución automática y se realiza la acción especificada por **ShellExecute** , tal y como se describió anteriormente. (Tenga en cuenta que solo AutoRun está disponible en versiones de Windows anteriores a Windows XP).
-   En Windows XP, la entrada **UseAutoPlay** hace que se use la reproducción automática en lugar de la ejecución automática. En este caso, la reproducción automática determina que el medio contiene un archivo Windows Media Audio (. WMA) y clasifica el contenido como "archivos de música". Se presenta al usuario un cuadro de diálogo de reproducción automática que contiene controladores registrados para el tipo de medio de reproducción automática "archivos de música"; se omite la entrada ShellExecute de ejecución automática.

### <a name="shellexecute"></a>shellexecute

[Versión 5,0.](versions.md) La entrada **ShellExecute** especifica una aplicación o un archivo de datos que Autorun usará para llamar a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Parámetros

-   *filepath*

    Cadena que contiene la ruta de acceso completa del directorio que contiene los datos o el archivo ejecutable. Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.

-   *filename*

    Cadena que contiene el nombre del archivo. Si es un archivo ejecutable, se inicia. Si es un archivo de datos, debe ser miembro de un tipo de [archivo](fa-file-types.md). [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) inicia el comando predeterminado asociado al tipo de archivo.

-   *paramx*

    Contiene los parámetros adicionales que se deben pasar a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

### <a name="remarks"></a>Observaciones

Esta entrada es similar a [abrir](#parameters), pero le permite usar la información de [Asociación de archivos](fa-intro.md) para ejecutar la aplicación.

### <a name="shell"></a>shell

La entrada de **Shell** especifica un comando predeterminado para el menú contextual de la unidad.


```
shell=verb
```



### <a name="parameters"></a>Parámetros

-   *Verbo*

    Verbo que corresponde al comando de menú. El verbo y su comando de menú asociado deben definirse en el archivo Autorun. inf con una entrada de [ \\ verbo de Shell](#shellverb) .

### <a name="remarks"></a>Observaciones

Cuando un usuario hace clic con el botón secundario en el icono de la unidad, aparece un menú contextual. Si hay un archivo Autorun. inf, se toma el comando de menú contextual predeterminado. Este comando también se ejecuta cuando el usuario hace doble clic en el icono de la unidad.

Para especificar el comando de menú contextual predeterminado, defina primero el verbo, la cadena de comando y el texto de menú con el [ \\ verbo de Shell](#shellverb). A continuación, use Shell para convertirlo en el comando de menú contextual predeterminado. De lo contrario, el texto del elemento de menú predeterminado será "reproducción automática", que inicia la aplicación especificada por la entrada [abierta](#parameters) .

### <a name="shellverb"></a>verbo de Shell \\

La entrada de **\\ verbo de Shell** agrega un comando personalizado al menú contextual de la unidad.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Parámetros

-   *Verbo*

    Verbo del comando de menú. La entrada de *_\\ comando_* de _verbo_ de **Shell \\** asocia el verbo con un archivo ejecutable. Los verbos no deben contener espacios incrustados. De forma predeterminada, *Verb* es el texto que se muestra en el menú contextual.

-   *Filename.exe*

    Ruta de acceso y nombre de archivo de la aplicación que realiza la acción.

-   *MenuText*

    Este parámetro especifica el texto que se muestra en el menú contextual. Si se omite, se muestra el *verbo* . *MenuText* puede ser una combinación de mayúsculas y minúsculas y puede contener espacios. Puede establecer una tecla de método abreviado para el elemento de menú colocando una y comercial (&) delante de la letra.

### <a name="remarks"></a>Observaciones

Cuando un usuario hace clic con el botón secundario en el icono de la unidad, aparece un menú contextual. La adición de entradas de **\\ verbo de Shell** al archivo Autorun. inf de la unidad permite agregar comandos a este menú contextual.

Esta entrada tiene dos partes, que deben estar en líneas independientes. La primera parte es el *_\\ comando_* de _verbo_ de **Shell \\**. Es obligatorio. Asocia una cadena, denominada *verbo*, a la aplicación para iniciar cuando se ejecuta el comando. La segunda parte es la entrada del _verbo_ de **Shell \\**. Es opcional. Puede incluirlo para especificar el texto que se muestra en el menú contextual.

Para especificar un comando de menú contextual predeterminado, defina el verbo con el **\\ verbo de Shell** y conviértalo en el comando predeterminado con la entrada de [Shell](#autoruninf-entries) .

En el fragmento siguiente de Autorun. inf de ejemplo se asocia el verbo *readit* a la cadena de comando "Notepad ABC \\readme.txt". El texto del menú es "Read Me" y "m" se define como la tecla de método abreviado del elemento. Cuando el usuario selecciona este comando, se abre el archivo dereadme.txt ABC de la unidad \\ con el Bloc de notas de Microsoft.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Claves de contenido \]

Hay tres claves de tipo de archivo: **MusicFiles**, **PictureFiles** y **videofiles**.

Si uno de estos contenidos se establece en true a través de uno de los valores 1, y, sí, t o true, la interfaz de usuario de reproducción automática muestra los controladores asociados a ese tipo de contenido, independientemente de si el contenido de ese tipo existe en el medio.

Si uno de estos contenidos se establece en false a través de uno de los valores 0, n, no, f o false, no distingue mayúsculas de minúsculas, la interfaz de usuario de reproducción automática no muestra los controladores asociados a ese tipo de contenido, aunque se detecte el contenido de ese tipo en el medio.

El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática. Por ejemplo, un CD se puede clasificar como que solo contenga contenido de música, aunque también tenga imágenes y vídeos y, de lo contrario, se vería como contenido mixto.

La sección de **\[ contenido \]** solo se admite en Windows Vista y versiones posteriores.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[Claves de ExclusiveContentPaths \]

Las carpetas que aparecen en esta sección limitan la reproducción automática para buscar solo las carpetas y las subcarpetas del contenido. Se pueden proporcionar con o sin una barra diagonal inversa ( \\ ). En cualquier caso, se toman como rutas de acceso absolutas del directorio raíz del medio. En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.

El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática y acortar el tiempo de examen limitando el análisis a ciertas áreas significativas del medio.

Todas las rutas de acceso válidas son las siguientes:


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



La sección **\[ ExclusiveContentPaths \]** solo se admite en Windows Vista y versiones posteriores.

## <a name="ignorecontentpaths-keys"></a>\[Claves de IgnoreContentPaths \]

La reproducción automática omite las carpetas que aparecen en esta sección y sus subcarpetas al buscar contenido en un medio. Se pueden proporcionar con o sin una barra diagonal inversa ( \\ ). En cualquier caso, se toman como rutas de acceso absolutas del directorio raíz del medio. En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.

Las rutas de acceso de esta sección tienen prioridad sobre las rutas de acceso de la sección **\[ ExclusiveContentPaths \]** . Si una ruta de acceso proporcionada en **\[ IgnoreContentPaths \]** es una subcarpeta de una ruta de acceso proporcionada en **\[ ExclusiveContentPaths \]**, se omitirá.

El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática y acortar el tiempo de examen limitando el análisis a ciertas áreas significativas del medio.

Todas las rutas de acceso válidas son las siguientes:


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



La sección **\[ IgnoreContentPaths \]** solo se admite en Windows Vista y versiones posteriores.

## <a name="deviceinstall-keys"></a>\[Claves de DeviceInstall \]

### <a name="driverpath"></a>DriverPath

La entrada **DriverPath** especifica un directorio para buscar archivos de controlador de forma recursiva. Este comando se usa durante la instalación de un controlador y no es parte de una operación de ejecución automática. La sección **\[ DeviceInstall \]** solo se admite en Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parámetros

-   *directoryPath*

    Una ruta de acceso a un directorio en el que Windows busca archivos de controlador, junto con todos sus subdirectorios.

### <a name="remarks"></a>Observaciones

No use Letras de unidad en *directoryPath* cuando cambien de un equipo a otro.

Para buscar en varios directorios, agregue una entrada **DriverPath** para cada directorio como en este ejemplo.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Si no se proporciona ninguna entrada **DriverPath** en la sección **\[ \] DeviceInstall** o la entrada **DriverPath** no tiene ningún valor, esa unidad se omite durante una búsqueda de archivos de controlador.

 

 
