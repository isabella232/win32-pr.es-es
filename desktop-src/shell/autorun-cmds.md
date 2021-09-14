---
description: Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun.inf. Una entrada consta de una clave y un valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas autorun.inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361061"
---
# <a name="autoruninf-entries"></a>Entradas autorun.inf

Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun.inf. Una entrada consta de una clave y un valor.

-   [\[Ejecutar claves \] automáticamente](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [icono](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [Shellexecute](#shellexecute)
    -   [Cáscara](#autoruninf-entries)
    -   [verbo \\ shell](#shellverb)
-   [\[Claves de \] contenido](#content-keys)
-   [\[Claves ExclusiveContentPaths \]](#exclusivecontentpaths-keys)
-   [\[Claves IgnoreContentPaths \]](#ignorecontentpaths-keys)
-   [\[DeviceInstall \] Keys](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[Ejecutar claves \] automáticamente

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [icono](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [Shellexecute](#shellexecute)
-   [Cáscara](#autoruninf-entries)
-   [verbo \\ shell](#shellverb)

### <a name="action"></a>action

La **entrada** de acción especifica el texto que se usa en el cuadro de diálogo Reproducción automática para el controlador que representa el programa especificado en la entrada [open](#parameters) o [shellexecute](#shellexecute) en el archivo Autorun.inf del medio. El valor se puede expresar como texto o como un recurso almacenado en un archivo binario.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parámetros

-   *ActionText*

    Texto que se usa en el cuadro de diálogo Reproducción automática para el controlador que representa el programa especificado en la entrada [open](#parameters) o [shellexecute](#shellexecute) en el archivo Autorun.inf del medio.

-   *Filepath*

    Cadena que contiene la ruta de acceso completa del directorio que contiene el archivo binario que contiene la cadena. Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.

-   *filename*

    Cadena que contiene el nombre del archivo binario.

-   *resourceID*

    Identificador de la cadena dentro del archivo binario.

### <a name="remarks"></a>Observaciones

La **clave** de acción solo se usa en Windows XP Service Pack 2 (SP2) o posterior. Solo se admite para unidades de tipo UNIDAD \_ EXTRAÍBLE y UNIDAD \_ FIJA. En el caso de DRIVE \_ REMOVABLE, se **requiere la** clave de acción. Se  omite un comando de acción en el archivo Autorun.inf de un CD de audio o DVD de película, y estos medios se siguen comportando como en Windows XP Service Pack 1 (SP1) y versiones anteriores.

La cadena que se muestra en el cuadro de diálogo Reproducción  automática se construye combinando el texto especificado en la entrada de acción con texto codificado de forma precisa que asigna al proveedor el nombre proporcionado por el Shell. El [icono](#parameters) se muestra junto a él. Esta entrada siempre aparece como la primera opción en el cuadro de diálogo Reproducción automática y está seleccionada de forma predeterminada. Si el usuario acepta la opción , se inicia la aplicación especificada por la entrada [open](#parameters) o [shellexecute](#shellexecute) en el archivo Autorun.inf del medio. La **opción Realizar siempre la acción seleccionada** no está disponible en esta situación.

Las [teclas de](#parameters) acción [e](#parameters) icono juntas definen la representación de la aplicación que ve el usuario final en el cuadro de diálogo Reproducción automática. Deben estar compuestos de tal manera que los usuarios puedan identificarlos fácilmente. Deben indicar la aplicación que se va a ejecutar, la empresa que la creó y cualquier personal de marca asociada.

Por compatibilidad con versiones anteriores, la **entrada de** acción es opcional para dispositivos de tipo DRIVE \_ FIXED. Para este tipo, se usa una entrada predeterminada en el cuadro de diálogo Reproducción automática si **no** hay ninguna entrada de acción en el archivo Autorun.inf.

La **entrada** de acción es obligatoria para los dispositivos de tipo DRIVE REMOVABLE, que hasta ahora no tenía \_ compatibilidad con Autorun.inf. Si no **hay ninguna** entrada de acción, se muestra el cuadro de diálogo Reproducción automática, pero sin opción para iniciar el contenido adicional.

### <a name="customevent"></a>CustomEvent

La **entrada CustomEvent** especifica un evento de contenido de Reproducción automática personalizado.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parámetros

-   *CustomEventName*

    Cadena de texto que contiene el nombre del evento de contenido de Reproducción automática. El nombre no debe tener más de 100 caracteres alfanuméricos.

### <a name="remarks"></a>Observaciones

Puede incluir un nombre de evento personalizado en el archivo Autorun.inf de un volumen. Cuando Reproducción automática solicita al usuario que una aplicación use con el volumen, solo muestra las aplicaciones que se han registrado para el nombre de evento personalizado especificado. Para obtener información sobre cómo puede registrar una aplicación como controlador para el evento de contenido de Reproducción automática personalizada, vea Inicio automático con [Reproducción](/previous-versions/windows/apps/hh452731(v=win.10)) automática o Registro de un [controlador de eventos.](how-to-register-an-event-handler.md)

En el ejemplo siguiente se especifica el valor "MyContentOnArrival" como un nuevo evento de contenido de Reproducción automática.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

La **entrada** de icono especifica un icono que representa la unidad habilitada para ejecución automática en la Windows usuario.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parámetros

-   *iconfilename*

    Nombre de un archivo .ico, .bmp, .exe o .dll que contiene la información del icono. Si un archivo contiene más de un icono, también debe especificar el índice de base cero del icono.

### <a name="remarks"></a>Observaciones

El icono, junto con la etiqueta , representa la unidad habilitada para ejecución automática en la Windows usuario. Por ejemplo, en Windows Explorer, la unidad se representa mediante este icono en lugar del icono de unidad estándar. El archivo del icono debe estar en el mismo directorio que el archivo especificado por el [comando open.](#parameters)

En el ejemplo siguiente se especifica el segundo icono del MyProg.exe archivo.


```
icon=MyProg.exe,1
```



### <a name="label"></a>etiqueta

La **entrada** de etiqueta especifica una etiqueta de texto que representa la unidad habilitada para ejecución automática en Windows interfaz de usuario.


```
label=LabelText
```



### <a name="parameters"></a>Parámetros

-   *LabelText*

    Cadena de texto que contiene la etiqueta. Puede contener espacios y no debe tener más de 32 caracteres.

> [!Note]  
> Es posible colocar un valor en el parámetro **LabelText** que supere los 32 caracteres y no reciba ningún mensaje de error. Sin embargo, el sistema solo muestra los primeros 32 caracteres. Los caracteres adicionales al 32 se truncan y no se muestran. Por ejemplo, si **LabelText** es el siguiente: label="Este CD está diseñado para ser el CD de música final". Se mostrará lo siguiente: "Este CD está diseñado para ser el ul".

 

### <a name="remarks"></a>Observaciones

La etiqueta, junto con un icono, representa la unidad habilitada para ejecución automática en la Windows usuario.

En el ejemplo siguiente se especifica el valor "Mi etiqueta de unidad" como etiqueta de la unidad.


```
label=My Drive Label
```



### <a name="open"></a>abierto

La **entrada** abierta especifica la ruta de acceso y el nombre de archivo de la aplicación que autorun se inicia cuando un usuario inserta un disco en la unidad.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parámetros

-   *exefile*

    Ruta de acceso completa de un archivo ejecutable que se ejecuta cuando se inserta el CD. Si solo se especifica un nombre de archivo, debe estar en el directorio raíz de la unidad. Para buscar el archivo en un subdirectorio, debe especificar una ruta de acceso. También puede incluir uno o varios parámetros de línea de comandos para pasar a la aplicación de inicio.

### <a name="useautoplay"></a>UseAutoPlay

En Windows XP, la **entrada UseAutoPlay** especifica que se debe usar Reproducción automática en lugar de Ejecutar automáticamente.

En Windows Vista y versiones posteriores, esta entrada hace que las acciones especificadas para AutoRun (mediante las entradas **open** o **shellexecute)** se supriman del cuadro de diálogo Reproducción automática. Esta entrada no tiene ningún efecto en las versiones de Windows anteriores a Windows XP.

En Windows 8 y versiones posteriores, al especificar un valor de 0 se deshabilitará la reproducción automática para este dispositivo.

### <a name="parameters"></a>Parámetros

Para usar esta opción, agregue una entrada para **UseAutoPlay** al archivo Autorun.inf y establezca la entrada en 1. No se admite ningún otro valor en las versiones de Windows anteriores a Windows 8.

En Windows 8 y versiones posteriores, especifique un valor de 0 para deshabilitar la reproducción automática para este dispositivo.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Observaciones

Actualmente, **UseAutoPlay** solo se aplica en Windows XP o versiones posteriores y solo en una unidad que [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina que es de tipo **UNIDAD \_ CDROM**.

Cuando se usa **UseAutoPlay,** cualquier  acción especificada por las entradas open o **shellexecute** en Autorun.inf se omite en Windows XP y se omite en el cuadro de diálogo Reproducción automática en Windows Vista.

AutoRun se usa normalmente para ejecutar o cargar automáticamente algo contenido en el medio insertado, mientras que Reproducción automática presenta un cuadro de diálogo que incluye una lista de las acciones pertinentes que se pueden realizar y permite al usuario elegir qué acción realizar. Para obtener más información sobre la diferencia entre AutoRun y AutoPlay, vea Creating [an AutoRun-enabled CD-ROM Application](autoplay.md) y [Using and Configuring AutoPlay](autoplay2k-using.md), respectivamente.

### <a name="usage-example"></a>Ejemplo de uso

Un CD contiene tres archivos: Autorun.inf, Readme.txt y Música.wma. Según la versión de Windows en uso y las opciones especificadas en Autorun.inf, el CD puede controlarse mediante AutoRun o AutoPlay cuando se inserta (suponiendo que AutoRun/AutoPlay esté habilitado para la unidad en la que se inserta el CD).

En primer lugar, considere un archivo Autorun.inf con el siguiente contenido, y tenga en cuenta que no se **especifica UseAutoPlay=1:**


```
[AutoRun]
shellexecute="Readme.txt"
```



La acción realizada por shell cuando se inserta este CD depende de la versión de Windows en uso:

-   En Windows XP o versiones anteriores, autoejecución controla este CD cuando se inserta. En este caso, se lee **la entrada shellexecute** y shell invoca el controlador de archivos asociado a .txt archivos; normalmente esto abriría Readme.txt en Bloc de notas.
-   En Windows Vista, la presencia de un archivo Autorun.inf con una entrada **shellexecute** hace que el medio se identifique como tipo de reproducción automática "Software y juegos". En este caso, se presenta al usuario un cuadro de diálogo Reproducción automática que incluye la acción especificada por la entrada **shellexecute** (presentada como "Cargar Readme.txt" en el cuadro de diálogo), junto con acciones predeterminadas asociadas a medios de tipo "Software y juegos".

Para indicar que se debe usar Reproducción automática en lugar de Ejecutar automáticamente en Windows XP y que la acción especificada por la entrada AutoRun shellexecute debe suprimirse desde el cuadro de diálogo Reproducción automática en Windows Vista, inserte **UseAutoPlay** en el archivo Autorun.inf como se indica a continuación:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



Una vez más, la acción realizada por shell cuando se inserta este CD depende de la versión de Windows en uso.

-   En las versiones de Windows anteriores a Windows XP, se sigue utilizando AutoRun y se realiza la acción especificada por **shellexecute,** como se ha descrito anteriormente. (Tenga en cuenta que solo La ejecución automática está disponible en versiones de Windows anteriores a Windows XP).
-   En Windows XP, la **entrada UseAutoPlay** hace que AutoPlay se use en lugar de AutoRun. En este caso, Reproducción automática determina que el medio contiene un archivo Windows Media Audio (.wma) y clasifica el contenido como "Música archivos". El usuario aparece con un cuadro de diálogo Reproducción automática que contiene controladores registrados para el tipo de medio "Música archivos". La entrada AutoRun shellexecute se omite.

### <a name="shellexecute"></a>shellexecute

[Versión 5.0.](versions.md) La **entrada shellexecute** especifica una aplicación o un archivo de datos que AutoRun usará para llamar a [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Parámetros

-   *Filepath*

    Cadena que contiene la ruta de acceso completa del directorio que contiene los datos o el archivo ejecutable. Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.

-   *filename*

    Cadena que contiene el nombre del archivo. Si es un archivo ejecutable, se inicia. Si es un archivo de datos, debe ser miembro de un tipo [de archivo](fa-file-types.md). [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) inicia el comando predeterminado asociado al tipo de archivo.

-   *paramx*

    Contiene los parámetros adicionales que se deben pasar a [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

### <a name="remarks"></a>Observaciones

Esta entrada es similar [a abrir](#parameters), pero permite usar información de asociación [de](fa-intro.md) archivos para ejecutar la aplicación.

### <a name="shell"></a>shell

La **entrada del** shell especifica un comando predeterminado para el menú contextual de la unidad.


```
shell=verb
```



### <a name="parameters"></a>Parámetros

-   *Verbo*

    Verbo que corresponde al comando de menú. El verbo y su comando de menú asociado deben definirse en el archivo Autorun.inf con una entrada [ \\ de verbo de](#shellverb) shell.

### <a name="remarks"></a>Observaciones

Cuando un usuario hace clic con el botón derecho en el icono de unidad, aparece un menú contextual. Si hay un archivo Autorun.inf, el comando de menú contextual predeterminado se toma de él. Este comando también se ejecuta cuando el usuario hace doble clic en el icono de la unidad.

Para especificar el comando de menú contextual predeterminado, defina primero su verbo, cadena de comando y texto de menú con [el \\ verbo de shell](#shellverb). A continuación, use shell para convertirla en el comando de menú contextual predeterminado. De lo contrario, el texto predeterminado del elemento de menú será "Reproducción automática", que inicia la aplicación especificada por la [entrada](#parameters) abierta.

### <a name="shellverb"></a>verbo \\ shell

La **entrada \\ del verbo** de shell agrega un comando personalizado al menú contextual de la unidad.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Parámetros

-   *Verbo*

    Verbo del comando de menú. La **\\ entrada del**_comando_*_\\ del verbo_* de shell asocia el verbo a un archivo ejecutable. Los verbos no deben contener espacios incrustados. De forma predeterminada, *verbo* es el texto que se muestra en el menú contextual.

-   *Filename.exe*

    Ruta de acceso y nombre de archivo de la aplicación que realiza la acción.

-   *MenuText*

    Este parámetro especifica el texto que se muestra en el menú contextual. Si se omite, se *muestra* el verbo . *MenuText* puede ser de mayúsculas y minúsculas mixtas y puede contener espacios. Puede establecer una tecla de método abreviado para el elemento de menú colocando una y comercial (&) delante de la letra.

### <a name="remarks"></a>Observaciones

Cuando un usuario hace clic con el botón derecho en el icono de unidad, aparece un menú contextual. Agregar **entradas \\ de verbo** de shell al archivo Autorun.inf de la unidad permite agregar comandos a este menú contextual.

Hay dos partes en esta entrada, que deben estar en líneas independientes. La primera parte es el **comando \\ del** verbo _de_*_\\ shell_*. Es obligatorio. Asocia una cadena, denominada *verbo*, a la aplicación que se va a iniciar cuando se ejecuta el comando. La segunda parte es la entrada **del verbo \\ de** shell. Es opcional. Puede incluirlo para especificar el texto que se muestra en el menú contextual.

Para especificar un comando de menú contextual predeterminado, defina el verbo con el **verbo de \\ shell** y conséctelo como el comando predeterminado con la entrada [del](#autoruninf-entries) shell.

El fragmento Autorun.inf de ejemplo siguiente asocia el verbo *readit* con la cadena de comandos "Bloc de notas abc \\readme.txt". El texto del menú es "Léame" y "M" se define como la tecla de método abreviado del elemento. Cuando el usuario selecciona este comando, se abre el archivo abc \\readme.txt de la unidad con Microsoft Bloc de notas.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Claves de \] contenido

Hay tres claves de tipo de archivo: **MusicFiles**, **PictureFiles** y **VideoFiles.**

Si uno de estos contenidos se establece en true a través de uno, los valores 1, y, sí, t o true no distinción entre mayúsculas y minúsculas, la interfaz de usuario reproducción automática muestra los controladores asociados a ese tipo de contenido independientemente de si el contenido de ese tipo existe en el medio.

Si uno de estos contenidos se establece en false a través de uno, los valores 0, n, no, f o false que no tienen en cuenta mayúsculas de minúsculas, la interfaz de usuario de Reproducción automática no muestra los controladores asociados a ese tipo de contenido aunque se detecte contenido de ese tipo en el medio.

El uso de esta sección está pensado para permitir que los autores de contenido comuniquen la intención del contenido a Reproducción automática. Por ejemplo, un CD se puede clasificar como que contiene solo contenido de música, aunque también tenga imágenes y vídeos y, de lo contrario, se vería como contenido mixto.

La **\[ sección \]** Contenido solo se admite en Windows Vista y versiones posteriores.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[Claves ExclusiveContentPaths \]

Las carpetas enumeradas en esta sección limitan la reproducción automática a la búsqueda de contenido solo en esas carpetas y sus subcarpetas. Se pueden dar con o sin una barra diagonal inversa inicial ( \\ ). En cualquier caso, se toman como rutas de acceso absolutas desde el directorio raíz del medio. En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.

El uso de esta sección está pensado para permitir que los autores de contenido comuniquen la intención del contenido a Reproducción automática y reduzcan su tiempo de examen limitando el examen a determinadas áreas importantes de los medios.

A continuación se den todas las rutas de acceso válidas


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



La **\[ sección ExclusiveContentPaths \]** solo se admite en Windows Vista y versiones posteriores.

## <a name="ignorecontentpaths-keys"></a>\[Claves IgnoreContentPaths \]

La reproducción automática omite las carpetas enumeradas en esta sección y sus subcarpetas al buscar contenido en un medio. Se pueden dar con o sin una barra diagonal inversa inicial ( \\ ). En cualquier caso, se toman como rutas de acceso absolutas desde el directorio raíz del medio. En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.

Las rutas de acceso de esta sección tienen prioridad sobre las **\[ rutas de acceso de la \] sección ExclusiveContentPaths.** Si una ruta de acceso especificada **\[ en IgnoreContentPaths \]** es una subcarpeta de una ruta de acceso especificada en **\[ ExclusiveContentPaths \]**, todavía se omite.

El uso de esta sección está pensado para permitir que los autores de contenido comuniquen la intención del contenido a Reproducción automática y reduzcan su tiempo de examen limitando el examen a determinadas áreas importantes de los medios.

A continuación se den todas las rutas de acceso válidas


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



La **\[ sección IgnoreContentPaths \]** solo se admite en Windows Vista y versiones posteriores.

## <a name="deviceinstall-keys"></a>\[DeviceInstall \] Keys

### <a name="driverpath"></a>DriverPath

La **entrada DriverPath** especifica un directorio para buscar archivos de controlador de forma recursiva. Este comando se usa durante la instalación de un controlador y no forma parte de una operación de ejecución automática. La **\[ sección \] DeviceInstall** solo se admite en Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parámetros

-   *directorypath*

    Ruta de acceso a un directorio que Windows busca archivos de controlador, junto con todos sus subdirectorios.

### <a name="remarks"></a>Observaciones

No use letras de unidad en *directorypath* a medida que cambien de un equipo al siguiente.

Para buscar varios directorios, agregue una **entrada DriverPath** para cada directorio como en este ejemplo.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Si no se proporciona ninguna entrada **DriverPath** en la sección **\[ DeviceInstall \]** o la entrada **DriverPath** no tiene ningún valor, esa unidad se omite durante una búsqueda de archivos de controlador.

 

 
