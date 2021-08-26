---
description: Storage de cadenas codificadas de forma fuerte en el Registro forma parte de un modelo de localización Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Uso del redireccionamiento de cadenas del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bac55f59bd414002f5dcc0ce3611102a4effd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887405"
---
# <a name="using-registry-string-redirection"></a>Uso del redireccionamiento de cadenas del Registro

Storage de cadenas codificadas de forma fuerte en el Registro forma parte de un modelo de localización Windows Vista. NO es compatible con MUI. En el modelo actual, la interfaz de usuario del sistema operativo se ejecuta en archivos de recursos específicos del idioma sobre una base neutra del idioma. Los componentes del sistema operativo usan el Registro de manera neutra en el idioma.

LDAP solo usa cadenas del Registro redirigidas definidas por recursos de Win32 PE en el archivo de recursos del lenguaje base. El redireccionamiento se define por separado, por ejemplo, en un archivo .inf. Este tipo de almacenamiento permite al cargador de recursos seleccionar automáticamente los recursos de lenguaje correctos durante la carga del módulo de recursos.

> [!Note]  
> Este tema solo pertenece a los recursos de Win32 PE. Si usa recursos pe que no son de Win32, debe proporcionar un redireccionamiento de cadenas del Registro personalizado, si es necesario.

 

## <a name="create-a-language-neutral-resource"></a>Creación de un Language-Neutral recurso

Una aplicación DEI que se ejecuta en Windows Vista y versiones posteriores usa un recurso de cadena neutral del lenguaje para permitir el acceso a cadenas específicas del idioma almacenadas en una tabla de recursos de cadena. El código de aplicación que lee estos valores del Registro se describe en la sección Cargar un Language-Neutral valor del Registro de [Buscar cadenas redirigidas.](locating-redirected-strings.md)

Los datos de un valor de registro con idioma neutro tienen el formato `@<PE-path>,-<stringID>[;<comment>]` " ", donde:

-   *PE-path* especifica la ruta de acceso del ejecutable. Puede especificar la ruta de acceso mediante una variable de entorno, como %ProgramFiles%, para admitir la implementación. Una alternativa para hacer referencia a la cadena es dejar fuera la información de la ruta de acceso del archivo. En este caso, la aplicación debe tener algunos medios, por ejemplo, otro valor del Registro, para comunicar su propio directorio de instalación.
-   *stringID* especifica el identificador numérico del recurso de cadena pertinente, que se implementa igual que cualquier otro recurso de cadena localizable.
-   *comment* especifica información opcional para la depuración o legibilidad del valor del Registro. Las funciones de API del Registro omiten el comentario al cargar la cadena.

> [!Note]  
> Los datos del valor del Registro no hacen referencia explícita al archivo de recursos específico del lenguaje. El archivo correcto se determina en tiempo de ejecución, en función de las preferencias actuales del lenguaje de la interfaz de usuario.

 

Se introduce un valor del Registro sin espacio entre "," y "-". Un valor correcto del Registro es:

`shell32.dll,-22912`

Un valor incorrecto del Registro es:

`shell32.dll, -22912`

Un ejemplo de Windows Vista es el valor del Registro con los datos siguientes:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Crear recursos para cadenas de acceso directo

Cuando la aplicación DEA muestra su nombre en la interfaz de usuario del shell, se muestra una cadena de información sobre el icono de la aplicación. Debe crear recursos de cadena para el nombre para mostrar de la aplicación y la cadena de información sobre información asociada para cada idioma admitido. Cuando los recursos estén listos, la aplicación puede usar las cadenas como se describe en La API de Shell para cargar cadenas de acceso directo desde la sección Registro de [Buscar cadenas redirigidas.](locating-redirected-strings.md)

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Preparar recursos para un acceso directo creado con Windows instalador

Si usa el instalador Windows (MSI) para crear un acceso directo, los recursos de cadena incluyen el nombre para mostrar y la descripción del acceso directo. En la [tabla de](../msi/shortcut-table.md)métodos abreviados MSI , se hace referencia al archivo DLL de recursos en las columnas adecuadas y los identificadores de recursos del nombre para mostrar y la descripción del acceso directo se usan en las columnas de identificador de recursos correspondientes.

Para que el acceso directo de la aplicación funcione correctamente con la tecnología de recursos de MUI, tenga en cuenta los siguientes puntos al preparar las cadenas de acceso directo:

-   Use variables de entorno o una ruta de acceso relativa para registrar el archivo DLL. Puede especificar @%systemroot% system32shell32.dll siempre que el tipo de cadena del \\ Registro sea REG EXPAND \\ \_ \_ SZ. El identificador de recurso de cadena para "Documento de texto" Shell32.dll es 12345.
-   No use espacios alrededor de los símbolos "," y "-". Un ejemplo correcto es "shell32.dll,-22912".
-   No use un nombre de archivo corto. Este tipo de nombre no funciona con el cargador de recursos.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparar recursos para un acceso directo mediante el formato INF

Si usa el formato de archivo INF para crear cadenas de acceso directo, el archivo de recursos debe realizar la siguiente configuración del Registro. En estas instrucciones se da por supuesto el uso de la sintaxis ProfileItems de setup API.

1.  Cambie el valor de Información sobre información para que apunte a la referencia de redireccionamiento de cadenas, mediante la ruta de acceso y el identificador de recurso.
2.  Agregue el nuevo valor DisplayResource en las secciones de instalación profileItems.

A continuación se muestra un ejemplo en el que se muestra la adición de la aplicación Calculadora al **menú** Inicio:


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Use la sintaxis que se muestra a continuación al usar INF para agregar elementos, por ejemplo, una carpeta Grupo de acceso, al **menú** Inicio. Esta sintaxis supone el uso de la compatibilidad con StartMenuItems del programa de instalación, similar a la \[ \] sintaxis usada en Syssetup.inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Establezca la información *sobre el valor* en la referencia de cadena " `@<path>,-resID` ".

El nombre para mostrar viene determinado por los *valores resDLL* *y resID.* El *valor resID* especifica el identificador de recurso para un recurso de cadena asociado al archivo neutral del idioma. El *valor resDLL* especifica la ruta de acceso al archivo neutro del idioma.

## <a name="create-resources-for-friendly-document-type-names"></a>Crear recursos para nombres de tipo de documento descriptivos

Debe implementar cadenas de nombre descriptivo e información sobre la información para la aplicación como recursos de cadena. Para permitir que los nombres de tipo de documento descriptivos reaccionen al lenguaje de la interfaz de usuario, la aplicación debe registrar los nombres mediante el valor FriendlyTypeName en la clave de identificador de programa para el tipo de archivo. El valor predeterminado de la clave de identificador de programa debe conservarse para mantener la compatibilidad con versiones anteriores. Para obtener información sobre cómo obtener acceso a los nombres de la aplicación, vea Query Friendly Document Type Names (Nombres de tipo de documento descriptivos para consultas) en la sección Registro de [Buscar cadenas redirigidas.](locating-redirected-strings.md)

El trabajo específico implica los pasos siguientes:

1.  Implemente el nombre descriptivo y las cadenas de información sobre información como recursos de cadena específicos del lenguaje.
2.  Agregue el valor FriendlyTypeName en la clave del Registro del tipo de documento. Los datos del valor siguen el patrón " ", donde path indica que el ejecutable y `@<path>,-<resID>` *resID* es el identificador de recursos de un recurso de cadena localizable asociado a ese ejecutable. 
3.  Especifique el valor del Registro de Información sobre información según el formato " `@<path>,-<resID>` ".

En el ejemplo siguiente se muestra la configuración del Registro para un .txt archivo:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Proporcionar recursos para las cadenas de acción del verbo shell

Las cadenas de acción para determinados verbos, por ejemplo, "open" y "edit", se muestran en el menú emergente que se muestra cuando el usuario hace clic con el botón derecho en un archivo en Windows Explorer. La aplicación no tiene que especificar cadenas para verbos de shell comunes, ya que el shell tiene sus propios valores predeterminados habilitados para MUI para estos verbos. Sin embargo, debe proporcionar recursos de cadena localizables para las cadenas que representan verbos poco comunes.

En sistemas operativos xp Windows, las cadenas de los verbos de shell en el Registro se representan con la sintaxis siguiente, donde *el* verbo especifica el nombre del verbo real:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Este es un ejemplo:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



En Windows XP y versiones posteriores, puede usar un nivel de direccionamiento indirecto para que una cadena de acción dependa del lenguaje de la interfaz de usuario. Estos sistemas operativos admiten un valor DEVERB para la definición de una cadena compatible con MUI. Este es un ejemplo de una entrada del Registro para un verbo poco común:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



La aplicación DEA también debe poder registrar el valor predeterminado anterior como una cadena localizable, como se muestra a continuación:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> No se recomienda el registro del valor predeterminado anterior porque requiere una configuración diferente en Windows XP y versiones posteriores de la que se usó en sistemas operativos anteriores.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Crear recursos para cadenas Verb, Protocol y AuxUserType

Debe crear recursos de cadena localizables para las cadenas Verb, Protocol y AuxUserType. Use la siguiente configuración del Registro:


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



El valor especificado para LocalizedString solo contiene o reemplaza el valor de *Verbo,* no los dos valores de marca.

Este es un resumen que le ayudará a garantizar la configuración correcta del Registro:

-   Si CLSID tiene una clave INSERTABLE HKCR CLSID {clsid}, defina el valor predeterminado de \\ \\ CLSID mediante \\ HKCR \\ CLSID \\ {clsid} \\ LocalizedString.
-   Si CLSID tiene una o varias subclaves en el verbo HKCR \\ CLSID {clsid}, defina cada cadena de verbo individual mediante \\ \\ HKCR \\ CLSID \\ {clsid} \\ Verb xxx \\ \\ LocalizedString.
-   Si CLSID tiene una o varias subclaves en HKCR {progid} Protocol Stdfileediting Verb, defina cada cadena de verbo individual mediante \\ \\ \\ \\ HKCR \\ {progid} \\ Protocol \\ Stdfileediting \\ Verb xxx \\ \\ LocalizedString.
-   Si CLSID tiene una o varias subclaves AuxiliarUserType enumeradas en HKCR \\ CLSID \\ {clsid} AuxUserType, defina cada entrada \\ de AuxUserType mediante HKCR \\ CLSID \\ {clsid} \\ AuxUserType \\ xxx \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Crear un recurso para el programa de desinstalación

Para registrar el programa de desinstalación de la aplicación, puede crear valores del Registro en la subclave de identificador único de la aplicación en la clave del Registro HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Uninstall. Los valores que se deben establecer son: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Para habilitar la tecnología DEA para cada valor, puede anexar \_ "Localizado" al nombre del valor.

 

Los componentes del sistema operativo son necesarios para proporcionar un valor para DisplayName \_ Localizado de una manera específica de MUI. Debe colocar el nombre para mostrar en un archivo DLL, como Res.dll, como un recurso de cadena, suponiendo que el identificador sea 1245. A continuación, la aplicación puede registrar el nombre para mostrar como DisplayName Localized con el valor \_ "@ \\res.DLL,-1245". Todas las demás configuraciones del Registro deben conservarse tal y como están, incluido el valor original de DisplayName.

## <a name="create-resources-for-sound-events"></a>Creación de recursos para eventos de sonido

Windows ciertos eventos con archivos de sonido, por ejemplo, un evento de notificación de correo nuevo o un evento de alarma de batería crítica. La interfaz de usuario debe mostrar los nombres de evento y debe admitir la globalización. Por lo tanto, debe implementar un recurso de cadena localizable para la descripción de cada descripción del evento. Agregue un nuevo valor del Registro para cada nombre de evento, además del valor predeterminado codificado de forma predeterminada.

Haga lo siguiente para habilitar un evento de sonido:

1.  Implemente la descripción como un recurso de cadena localizable.
2.  Agregue un nuevo valor del Registro para el nombre para mostrar, además del valor predeterminado codificado de forma hard-coded. A continuación se muestra el diseño del Registro asociado:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Si el shell no puede encontrar o recuperar el valor de DispFileName, usa la descripción predeterminada.

## <a name="create-resources-for-keyboard-layout-strings"></a>Crear recursos para cadenas de diseño de teclado

Si la aplicación implementa un diseño de teclado, requiere un recurso de cadena localizable para el nombre del diseño para la presentación de pantalla, por ejemplo, en listas de diseños de teclado. Cada diseño de teclado tiene una clave del Registro en HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control Keyboard \\ Layouts (Diseños de teclado del control HKEY LOCAL MACHINE System).

Entre los valores de esa clave se encuentran Texto de diseño, un nombre legible para la compatibilidad con versiones anteriores y Nombre para mostrar de diseño. Los datos proporcionados para Layout Display Name deben ser una referencia de cadena con el formato " ", que hace referencia a un recurso de cadena localizable asociado al `@<path>,-resID` diseño del teclado.

Este es un ejemplo de una configuración del Registro para el diseño de teclado español (España):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Representar cadenas de diálogo comunes de objetos de inserción OLE

Puede implementar el nombre para mostrar de un objeto insertable OLE como un recurso de cadena localizable asociado al código que implementa ese objeto. El [cuadro de diálogo Objeto](/cpp/mfc/reference/coleinsertdialog-class) de inserción OLE obtiene un nombre para mostrar de la clave del Registro HKCR \\ CLSID { \\ *&lt; GUID &gt;*}, donde *GUID* identifica el identificador de clase de un objeto OLE insertable. Windows Vista y versiones posteriores implementan este tipo de objeto de una manera localizable, mediante un nombre para mostrar compatible con HIPAA que permite la personalización en el lenguaje de interfaz de usuario. En cambio, los sistemas operativos Windows Vista implementan el nombre para mostrar para este tipo de objeto utilizando el valor predeterminado de la clave del Registro correspondiente. Normalmente, este nombre es un nombre en inglés (Estados Unidos) o un nombre en el idioma de interfaz de usuario predeterminado del sistema.

> [!Note]  
> No todos los objetos que corresponden a subclaves de la clave del Registro son insertables.

 

El valor predeterminado de la clave HKCR \\ CLSID \\ {*&lt; GUID &gt;*} debe conservar un nombre legible para la compatibilidad con versiones anteriores. Sin embargo, también debe definir el valor LocalizedString, con el formato " ", donde path identifica el `@<path>,-ResID` archivo ejecutable que implementa el objeto . El valor ResID especifica el identificador de recurso de la cadena localizable para el nombre para mostrar.

Por ejemplo, el script de registro para el objeto Clip multimedia insertable incluye las líneas siguientes:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



La primera línea proporciona compatibilidad con versiones anteriores colocando una cadena de texto simple en el Registro como un nombre para mostrar predeterminado. La segunda línea proporciona acceso al nombre para mostrar compatible con HIPAA. Indica el identificador de cadena almacenado en Mplay32.exe. La cadena con el identificador 9217 en Mplay32.exe se puede asociar a valores de recursos de cadena para cualquier número de idiomas. Su nombre en inglés (Estados Unidos) es "Clip multimedia".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Crear recursos de cadena para Microsoft Management Console Snap-Ins

Debe crear un recurso de cadena localizable para cada Microsoft Management Console complemento mmc (MMC) que usa la aplicación DE INS. Dado que un complemento forma parte de una consola, tiene una interfaz de usuario y debe globalizarse para funcionar en más de un idioma.

En su mayor parte, los complementos MMC emiten los mismos problemas de globalización y localización que la propia aplicación DE EXTENSIÓN. Un complemento MMC debe reflejar su nombre en el Registro para mostrarlo. La entrada del Registro debe incluir una referencia indirecta a un recurso de cadena localizable y una cadena literal para la compatibilidad con versiones anteriores.

Cada complemento MMC tiene una clave del Registro en HKEY \_ LOCAL MACHINE Software Microsoft \_ \\ \\ \\ MMC \\ SnapIns. Entre los valores de esa clave se encuentran NameString, que especifica un nombre legible para la compatibilidad con versiones anteriores, y NameStringIndirect, que especifica una referencia indirecta a un recurso de cadena localizable. Para NameStringIndirect, debe proporcionar una referencia de cadena con el formato " `@<path>,-resID` ", que representa un recurso de cadena localizable.

Por ejemplo, puede establecer la siguiente configuración para Mymmc.dll, donde 12345 es el identificador del recurso de cadena correspondiente que contiene el nombre localizable del complemento:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Algunos complementos registran otros valores de cadena del Registro que MMC no lee del Registro. Para obtener más información sobre el uso de estos valores, vea Register Microsoft Management Console Snap-In Strings Not Read from the Registry en [Buscar cadenas redirigidas.](locating-redirected-strings.md)

## <a name="create-string-resources-for-a-windows-service"></a>Creación de recursos de cadena para un Windows service

Aunque un Windows normalmente tiene poca o ninguna interfaz de usuario, debe mostrar un nombre compatible con HIPAA y normalmente proporciona una descripción específica del lenguaje compatible con HIPAA. La clave del Registro que describe un servicio Windows admite solo el valor DisplayName para el nombre del servicio y el valor Description para la descripción del servicio.

Configuración para el servicio Windows se realizan desde la aplicación, como se describe en Establecer el nombre para mostrar y la descripción de un servicio Windows del Registro en Buscar [cadenas redirigidas.](locating-redirected-strings.md) Si la aplicación no establece los valores del Registro para la interfaz de usuario del servicio, los valores del Registro permanecen establecidos en inglés, incluso si la interfaz de usuario está en otro idioma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preparación de recursos](preparing-resources.md)
</dt> <dt>

[Buscar cadenas redirigidas](locating-redirected-strings.md)
</dt> </dl>

 

 
