---
description: El almacenamiento de cadenas codificadas de forma rígida en el registro forma parte de un modelo de localización anterior a Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Usar el redireccionamiento de cadenas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688692"
---
# <a name="using-registry-string-redirection"></a>Usar el redireccionamiento de cadenas del registro

El almacenamiento de cadenas codificadas de forma rígida en el registro forma parte de un modelo de localización anterior a Windows Vista. No es compatible con MUI. En el modelo actual, la interfaz de usuario del sistema operativo se ejecuta en archivos de recursos específicos del idioma encima de una base independiente del lenguaje. Los componentes del sistema operativo utilizan el registro de forma independiente del idioma.

MUI solo usa cadenas de registro redirigidas definidas por recursos PE de Win32 en el archivo de recursos de idioma base. La redirección se define por separado, por ejemplo, en un archivo. inf. Este tipo de almacenamiento permite al cargador de recursos seleccionar automáticamente los recursos de idioma correctos durante la carga del módulo de recursos.

> [!Note]  
> Este tema solo pertenece a los recursos de Win32 PE. Si utiliza recursos de PE que no son de Win32, debe proporcionar redirección de cadenas del registro personalizada, si es necesario.

 

## <a name="create-a-language-neutral-resource"></a>Creación de un recurso de Language-Neutral

Una aplicación MUI que se ejecuta en Windows Vista y versiones posteriores usa un recurso de cadena independiente del lenguaje para permitir el acceso a cadenas específicas del idioma almacenadas en una tabla de recursos de cadena. El código de la aplicación que lee estos valores del registro se describe en la sección carga de un valor de registro de Language-Neutral de [búsqueda de cadenas redirigidas](locating-redirected-strings.md).

Los datos de un valor del registro independiente del lenguaje tienen el formato " `@<PE-path>,-<stringID>[;<comment>]` ", donde:

-   *PE-path* especifica la ruta de acceso del archivo ejecutable. Puede especificar la ruta de acceso mediante una variable de entorno, como% ProgramFiles%, para admitir la implementación. Una alternativa para hacer referencia a la cadena es omitir la información de la ruta de acceso del archivo. En este caso, la aplicación debe tener algunos medios, por ejemplo, otro valor del registro, para comunicar su propio directorio de instalación.
-   *stringID* especifica el identificador de recursos numérico del recurso de cadena pertinente, que se implementa igual que cualquier otro recurso de cadena localizable.
-   *Comentario* especifica información opcional para la depuración o la legibilidad del valor del registro. Las funciones de la API del registro omiten el comentario al cargar la cadena.

> [!Note]  
> Los datos para el valor del registro no hacen referencia explícita al archivo de recursos específico del lenguaje. El archivo correcto se determina en tiempo de ejecución, según las preferencias de idioma de la interfaz de usuario actual.

 

Un valor del registro se escribe sin un espacio entre "," y "-". Un valor del registro correcto es:

`shell32.dll,-22912`

Un valor de registro incorrecto es:

`shell32.dll, -22912`

Un ejemplo de Windows Vista es el valor del registro con los datos siguientes:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Crear recursos para cadenas de acceso directo

Cuando la aplicación MUI muestra su nombre en la interfaz de usuario de Shell, se muestra una cadena de recuadro informativo para el icono de la aplicación. Debe crear recursos de cadena para el nombre para mostrar de la aplicación y la cadena de recuadro informativa asociada para cada idioma admitido. Cuando los recursos estén listos, la aplicación puede usar las cadenas tal y como se describe en la sección uso de la API de Shell para cargar cadenas de acceso directo desde el registro de [búsqueda de cadenas redirigidas](locating-redirected-strings.md).

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Preparar los recursos de un acceso directo creado con Windows Installer

Si usa Windows Installer (MSI) para crear un acceso directo, los recursos de cadena incluyen el nombre para mostrar y la descripción del método abreviado. En la [tabla de accesos directos MSI](../msi/shortcut-table.md), se hace referencia a la dll de recursos en las columnas adecuadas y se usan los identificadores de recursos para el nombre para mostrar y la descripción del acceso directo en las columnas de identificador de recursos correspondientes.

Para que el acceso directo de la aplicación funcione correctamente con la tecnología de recursos de MUI, tenga en cuenta los siguientes puntos al preparar las cadenas de acceso directo:

-   Use las variables de entorno o una ruta de acceso relativa para registrar el archivo DLL. Puede especificar @% SystemRoot% \\ system32shell32.dll siempre que \\ el tipo de cadena del registro sea reg \_ Expand \_ SZ. El identificador de recursos de cadena para "documento de texto" en Shell32.dll es 12345.
-   No use espacios alrededor de los símbolos "," y "-". Un ejemplo correcto es "shell32.dll,-22912".
-   No use un nombre de archivo corto. Este tipo de nombre no funciona con el cargador de recursos.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparar los recursos de un acceso directo mediante el formato INF

Si usa el formato de archivo INF para crear cadenas de acceso directo, el archivo de recursos debe tener la siguiente configuración del registro. En estas instrucciones se asume el uso de la sintaxis ProfileItems de la API de instalación.

1.  Cambie el valor de recuadro informativo para que apunte a la referencia de redirección de cadenas mediante la ruta de acceso y el identificador de recursos.
2.  Agregue el nuevo valor DisplayResource en las secciones de instalación ProfileItems.

El siguiente es un ejemplo que muestra la adición de la aplicación Calculator al menú **Inicio** :


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Use la sintaxis que se muestra a continuación al usar el archivo INF para agregar elementos, por ejemplo, una carpeta del grupo de acceso, al menú **Inicio** . Esta sintaxis presupone el uso de \[ la \] compatibilidad con StartMenuItems del programa de instalación, similar a la sintaxis usada en Syssetup. inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Establezca *el valor de* recuadro informativo en la referencia de cadena " `@<path>,-resID` ".

Los valores *resDLL* y *resID* determinan el nombre para mostrar. El valor *resID* especifica el identificador de recurso para un recurso de cadena asociado con el archivo independiente del idioma. El valor *resDLL* especifica la ruta de acceso al archivo independiente del idioma.

## <a name="create-resources-for-friendly-document-type-names"></a>Crear recursos para nombres descriptivos de tipos de documentos

Debe implementar las cadenas de nombre descriptivo y de recuadro informativo para la aplicación como recursos de cadena. Para permitir que los nombres de tipo de documento descriptivos reaccionen al idioma de la interfaz de usuario, la aplicación debe registrar los nombres mediante el valor FriendlyTypeName bajo la clave de identificador de programa para el tipo de archivo. El valor predeterminado de la clave de identificador de programa debe conservarse para mantener la compatibilidad con versiones anteriores. Para obtener información sobre cómo obtener acceso a los nombres de la aplicación, consulte los nombres de tipo de documento descriptivo de consulta en la sección registro de [Ubicación de cadenas redirigidas](locating-redirected-strings.md).

El trabajo específico conlleva los siguientes pasos:

1.  Implemente el nombre descriptivo y las cadenas de recuadro como recursos de cadena específicos del lenguaje.
2.  Agregue el valor FriendlyTypeName en la clave del registro de tipo de documento. Los datos para el valor siguen el patrón " `@<path>,-<resID>` ", donde *rutaDeAcceso* indica el archivo ejecutable y *resID* es el identificador de recurso de un recurso de cadena localizable asociado a ese ejecutable.
3.  Especifique el valor del registro informativo según el formato " `@<path>,-<resID>` ".

En el ejemplo siguiente se muestra la configuración del registro de un archivo. txt:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Proporcionar recursos para cadenas de acción de verbo de Shell

Las cadenas de acción para ciertos verbos, por ejemplo, "abrir" y "Editar", se muestran en el menú emergente que se muestra cuando el usuario hace clic con el botón secundario en un archivo en el explorador de Windows. La aplicación no tiene que especificar cadenas para los verbos de Shell comunes, ya que el shell tiene sus propios valores predeterminados habilitados para MUI para estos verbos. Sin embargo, debe proporcionar recursos de cadena localizable para las cadenas que representan verbos no comunes.

En los sistemas operativos anteriores a Windows XP, las cadenas de verbos de Shell del registro se representan con la sintaxis siguiente, donde *Verb* especifica el nombre de verbo real:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Este es un ejemplo:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



En Windows XP y versiones posteriores, puede usar un nivel de direccionamiento indirecto para que una cadena de acción dependa del idioma de la interfaz de usuario. Estos sistemas operativos admiten un valor MUIVerb para la definición de una cadena compatible con MUI. A continuación se muestra un ejemplo de una entrada del registro para un verbo no común:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



La aplicación MUI también debe poder registrar el valor predeterminado anterior como una cadena localizable, como se muestra a continuación:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> No se recomienda el registro del valor predeterminado anterior porque requiere una configuración diferente en Windows XP y versiones posteriores desde el programa de instalación usado en los sistemas operativos anteriores.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Crear recursos para cadenas de verbo, protocolo y AuxUserType

Debe crear recursos de cadena localizable para las cadenas de verbo, protocolo y AuxUserType. Utilice la siguiente configuración del registro:


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



El valor especificado para LocalizedString solo contiene o reemplaza el valor del *verbo*, no los dos valores de marca.

Este es un resumen para ayudarle a garantizar la correcta configuración del registro:

-   Si CLSID tiene una clave que se va a \\ Insertar en el CLSID HKCR \\ {CLSID} \\ , defina el valor de CLSID predeterminado mediante HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.
-   Si CLSID tiene una o más subclaves en \\ el \\ verbo HKCR CLSID {CLSID} \\ , defina cada cadena de verbo individual mediante HKCR \\ CLSID \\ {CLSID} \\ verbo \\ XXX \\ LocalizedString.
-   Si CLSID tiene una o más subclaves en el \\ verbo HKCR {ProgID} \\ Protocol \\ Stdfileediting \\ , defina cada cadena de verbo individual mediante HKCR \\ {ProgID} \\ Protocol \\ Stdfileediting \\ verbo \\ XXX \\ LocalizedString.
-   Si CLSID tiene una o más subclaves de AuxUserType enumeradas en HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, defina cada entrada de AuxUserType mediante HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ XXX \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Crear un recurso para el programa de desinstalación

Para registrar el programa de desinstalación de la aplicación, puede crear valores del registro en la subclave de identificador único de la aplicación en la clave del registro HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall. Entre los valores que se van a establecer se incluyen: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, comments, DisplayIcon, README, UrlUpdateInfo.

> [!Note]  
> Para habilitar la tecnología MUI para cada valor, puede anexar " \_ adaptado" al nombre del valor.

 

Los componentes del sistema operativo son necesarios para proporcionar un valor para DisplayName \_ adaptado en una forma específica de MUI. Debe colocar el nombre para mostrar en un archivo DLL, como Res.dll, como un recurso de cadena, suponiendo que el identificador sea 1245. A continuación, la aplicación puede registrar el nombre para mostrar como DisplayName \_ localizado con el valor "@ \\res.DLL,-1245". Todos los demás valores del registro deben conservarse tal como están, incluido el valor original de DisplayName.

## <a name="create-resources-for-sound-events"></a>Crear recursos para eventos de sonido

Windows asocia ciertos eventos con archivos de sonido, por ejemplo, un nuevo evento de notificación de correo o un evento de alarma de batería crítica. Los nombres de evento deben mostrarse en la interfaz de usuario y deben admitir la globalización. Por lo tanto, debe implementar un recurso de cadena localizable para la descripción de cada descripción del evento. Agregue un nuevo valor del registro para cada nombre de evento, además del valor predeterminado codificado de forma rígida.

Haga lo siguiente para habilitar un evento de sonido:

1.  Implemente la descripción como un recurso de cadena localizable.
2.  Agregue un nuevo valor del registro para el nombre para mostrar, además del valor predeterminado codificado de forma rígida. A continuación se muestra el diseño del registro asociado:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Si el shell no puede encontrar o recuperar el valor de DispFileName, utiliza la descripción predeterminada.

## <a name="create-resources-for-keyboard-layout-strings"></a>Crear recursos para cadenas de distribución de teclado

Si la aplicación implementa una distribución del teclado, requiere un recurso de cadena localizable como nombre del diseño para la presentación en pantalla, por ejemplo, en las listas de distribuciones del teclado. Cada distribución del teclado tiene una clave del registro en HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Keyboard Distributions.

Entre los valores de esa clave están el texto de diseño, un nombre legible para la compatibilidad con versiones anteriores y el nombre para mostrar del diseño. Los datos proporcionados para el nombre para mostrar del diseño deben ser una referencia de cadena con el formato " `@<path>,-resID` ", haciendo referencia a un recurso de cadena localizable asociado a la distribución del teclado.

Este es un ejemplo de una configuración del registro para la distribución del teclado español (España):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Representar cadenas de cuadro de diálogo comunes de objetos Insert OLE

Puede implementar el nombre para mostrar de un objeto OLE insertable como un recurso de cadena localizable asociado al código que implementa dicho objeto. El [cuadro de diálogo Insertar objeto OLE](/cpp/mfc/reference/coleinsertdialog-class) obtiene un nombre para mostrar de la clave del registro HKCR \\ CLSID \\ { *<GUID>* }, donde *GUID* identifica el identificador de clase de un objeto OLE insertable. Windows Vista y versiones posteriores implementan este tipo de objeto de forma localizable, utilizando un nombre para mostrar compatible con MUI que permite la personalización en el idioma de la interfaz de usuario. En cambio, los sistemas operativos anteriores a Windows Vista implementan el nombre para mostrar de este tipo de objeto utilizando el valor predeterminado de la clave del registro correspondiente. Normalmente, este nombre es un nombre en inglés (Estados Unidos) o un nombre en el idioma de la interfaz de usuario predeterminada del sistema.

> [!Note]  
> No se pueden insertar todos los objetos que corresponden a las subclaves de la clave del registro.

 

El valor predeterminado de la \\ clave HKCR CLSID \\ { *<GUID>* } debe conservar un nombre legible para la compatibilidad con versiones anteriores. Sin embargo, también debe definir el valor de LocalizedString, con el formato " `@<path>,-ResID` ", donde ruta de acceso identifica el archivo ejecutable que implementa el objeto. El valor ResID especifica el identificador de recurso de la cadena localizable para el nombre para mostrar.

Por ejemplo, el script de registro para el objeto de clip multimedia insertable incluye las siguientes líneas:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



La primera línea proporciona compatibilidad con versiones anteriores colocando una cadena de texto simple en el registro como un nombre para mostrar predeterminado. La segunda línea proporciona acceso al nombre para mostrar compatible con MUI. Indica el identificador de cadena almacenado en Mplay32.exe. La cadena con el identificador 9217 en Mplay32.exe se puede asociar a valores de recursos de cadena para cualquier número de lenguajes. Su nombre en inglés (Estados Unidos) es "clip multimedia".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Crear recursos de cadena para Microsoft Management Console Snap-Ins

Debe crear un recurso de cadena localizable para cada complemento de Microsoft Management Console (MMC) que usa la aplicación de MUI. Dado que un complemento es parte de una consola, tiene una interfaz de usuario y debe globalizarse para funcionar en más de un idioma.

En su mayor parte, los complementos MMC producen los mismos problemas de globalización y localización que la propia aplicación de MUI. Un complemento MMC debe reflejar su nombre en el registro para mostrarlo. La entrada del registro debe incluir una referencia indirecta a un recurso de cadena localizable y una cadena literal para mantener la compatibilidad con versiones anteriores.

Cada complemento MMC tiene una clave del registro en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MMC \\ complementos. Entre los valores de esa clave se NameString, especificando un nombre legible para la compatibilidad con versiones anteriores y NameStringIndirect, especificando una referencia indirecta a un recurso de cadena localizable. En el caso de NameStringIndirect, debe proporcionar una referencia de cadena con el formato " `@<path>,-resID` ", que representa un recurso de cadena localizable.

Por ejemplo, puede establecer la siguiente configuración para Mymmc.dll, donde 12345 es el identificador del recurso de cadena correspondiente que contiene el nombre traducible del complemento:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Algunos complementos registran otros valores de cadena del registro que MMC no lee del registro. Para obtener más información sobre el uso de estos valores, consulte registrar Microsoft Management Console Snap-In cadenas no leídas del registro en [localizar cadenas redirigidas](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Crear recursos de cadena para un servicio de Windows

Aunque un servicio de Windows normalmente tiene poca o ninguna interfaz de usuario, debe mostrar un nombre compatible con MUI y, normalmente, proporciona una descripción específica del lenguaje compatible con MUI. La clave del registro que describe un servicio de Windows solo admite el valor DisplayName para el nombre del servicio y el valor de descripción de la descripción del servicio.

La configuración del servicio de Windows se realiza desde la aplicación, tal y como se describe en establecer el nombre para mostrar y la descripción de un servicio de Windows desde el registro en [localizar cadenas redirigidas](locating-redirected-strings.md). Si la aplicación no establece los valores del registro para la interfaz de usuario del servicio, los valores del registro permanecen establecidos en inglés, aunque la interfaz de usuario esté en otro idioma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preparación de recursos](preparing-resources.md)
</dt> <dt>

[Localizar cadenas redirigidas](locating-redirected-strings.md)
</dt> </dl>

 

 
