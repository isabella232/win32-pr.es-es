---
description: La tabla de accesos directos contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabla de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910901"
---
# <a name="shortcut-table"></a>Tabla de acceso directo

La tabla de accesos directos contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.

La tabla de acceso directo tiene las columnas siguientes.



| Columna                 | Tipo                         | Clave | Nullable |
|------------------------|------------------------------|-----|----------|
| Acceso directo               | [Identificador](identifier.md) | Y   | N        |
| Directorio\_            | [Identificador](identifier.md) | N   | N        |
| Nombre                   | [Nombre de archivo](filename.md)     | N   | N        |
| Componente\_            | [Identificador](identifier.md) | N   | N        |
| Destino                 | [Acceso directo](shortcut.md)     | N   | N        |
| Argumentos              | [Formatea](formatted.md)   | N   | Y        |
| Descripción            | [Texto](text.md)             | N   | Y        |
| Tecla de acceso rápido                 | [Entero](integer.md)       | N   | Y        |
| Icono\_                 | [Identificador](identifier.md) | N   | Y        |
| IconIndex              | [Entero](integer.md)       | N   | Y        |
| ShowCmd                | [Entero](integer.md)       | N   | Y        |
| WkDir                  | [Identificador](identifier.md) | N   | Y        |
| DisplayResourceDLL     | [Formatea](formatted.md)   | N   | Y        |
| DisplayResourceId      | [Entero](integer.md)       | N   | Y        |
| DescriptionResourceDLL | [Formatea](formatted.md)   | N   | Y        |
| DescriptionResourceId  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Contextual
</dt> <dd>

Valor de clave de esta tabla.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

La clave externa en la primera columna de la [tabla de directorio](directory-table.md). Esta columna especifica el directorio en el que se crea el archivo de acceso directo.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre traducible del acceso directo que se va a crear.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

La clave externa en la primera columna de la [tabla de componentes](component-table.md). El instalador usa el estado de instalación del componente especificado en esta columna para determinar si se crea o se elimina el acceso directo. Este componente debe tener una ruta de acceso de clave válida para que se instale el acceso directo. Si la columna de destino contiene el nombre de una característica, el archivo Iniciado por el acceso directo es el archivo de clave del componente que se muestra en esta columna.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir
</dt> <dd>

El destino del acceso directo.

En el caso de un acceso directo anunciado, esta columna debe ser una clave externa en la primera columna de la [tabla de características](feature-table.md). El instalador evalúa la entrada en el campo de destino como un [identificador](identifier.md) y la entrada debe ser una clave externa válida en la [tabla de características](feature-table.md). El archivo Iniciado por el acceso directo en este caso es el archivo de clave del componente que aparece en la \_ columna componente. Cuando se activa el acceso directo, el instalador comprueba que todos los componentes de la característica se instalan antes de iniciar este archivo.

En el caso de un acceso directo no anunciado, el instalador evalúa este campo como una cadena [con formato](formatted.md) . El campo debe contener un identificador de propiedad entre corchetes ( \[ \] ), que se expande en el archivo o en una carpeta a la que apunta el acceso directo. Para obtener más información, consulte la [acción CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Argumentos de la línea de comandos para el acceso directo.

Tenga en cuenta que la resolución de propiedades en el campo arguments es limitada. Una propiedad con formato \[  \] de propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando se instala el componente que posee el acceso directo. Por ejemplo, para resolver el valor correcto para el argumento " \[ \#MyDoc.doc\] ", el mismo proceso debe instalar el archivo MyDoc.doc y el componente al que pertenece el acceso directo.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

La descripción localizable del acceso directo.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Directa
</dt> <dd>

Tecla de acceso rápido para el método abreviado. El byte de orden inferior contiene el código de clave virtual para la clave y el byte de orden superior contiene marcas de modificador. Debe ser un número no negativo. Por lo general, se recomienda que los autores de los paquetes de instalación no establezcan esta opción, ya que la configuración de esta opción puede Agregar teclas de error duplicadas al escritorio de un usuario. Además, la práctica de asignar teclas de acceso rápido a los accesos directos puede ser problemática para los usuarios que usan teclas de acceso directo para la [accesibilidad](accessibility.md).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

La clave externa para la columna uno de la [tabla de iconos](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice del icono para el acceso directo. Debe ser un número no negativo.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

El comando show para la ventana de la aplicación.

Se pueden usar los valores siguientes. Los valores son los definidos para la función de la API de Windows ShowWindow.



| Value | Significado             |
|-------|---------------------|
| 1     | \_SHOWNORMAL SW      |
| 3     | \_SHOWMAXIMIZED SW   |
| 7     | \_SHOWMINNOACTIVE SW |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Nombre de la propiedad que tiene la ruta de acceso del directorio de trabajo para el acceso directo. El valor puede utilizar el formato de Windows para hacer referencia a las variables de entorno, por ejemplo,% USERPROFILE%. Las referencias se resuelven en una ruta de acceso real cuando el instalador resuelve el directorio de trabajo para crear el acceso directo.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Este campo contiene un valor de cadena [con formato](formatted.md) para la ruta de acceso completa al archivo ejecutable portable (LN) independiente del idioma que contiene los datos de la configuración de recursos (RC config). La cadena con formato puede usar la \[ \# \] Convención filekey. Si este campo contiene un valor, se omite la columna Name. Si este campo está vacío, el instalador usa el valor de la columna nombre. Cuando este campo contiene un valor, el campo **DisplayResourceId** también es necesario para contener un valor o se produce un error en la instalación.

Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.

Para obtener información sobre cómo agregar accesos directos a la tabla de acceso directo para su uso con recursos de MUI, vea [un ejemplo de acceso directo de MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Índice del nombre para mostrar del acceso directo. Debe ser un número no negativo. Cuando este campo contiene un valor, el campo **DisplayResourceDLL** también es necesario para contener un valor o se produce un error en la instalación.

Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Este campo contiene un valor de cadena [con formato](formatted.md) para la ruta de acceso completa al archivo ejecutable portable (LN) independiente del idioma que contiene los datos de la configuración de recursos (RC config). La cadena con formato puede usar la \[ \# \] Convención filekey. Si este campo contiene un valor, se omite la columna Name. Si este campo está vacío, el instalador usa el valor de la columna Description. Cuando este campo contiene un valor, el campo **DescriptionResourceId** también es necesario para contener un valor o se produce un error en la instalación.

Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.

Para obtener información sobre cómo agregar accesos directos a la tabla de acceso directo para su uso con recursos de MUI, vea [un ejemplo de acceso directo de MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Índice del nombre de la descripción del acceso directo. Debe ser un número no negativo. Cuando este campo contiene un valor, el campo **DescriptionResourceDLL** también es necesario para contener un valor o se produce un error en la instalación.

Esta columna de la tabla de acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones de anteriores a Windows Installer 4,0.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La habilitación de una característica crea un acceso directo anunciado solo si la interfaz IShellLink del sistema admite la resolución de descriptores de instalador. Es compatible con Microsoft Windows 2000 y los sistemas que ejecutan Microsoft Internet Explorer 4,01. Si no se admite, el instalador crea un acceso directo no anunciado al instalar el componente de la característica, ya sea de forma local o se ejecuta desde el origen.

Tenga en cuenta que los accesos directos anunciados siempre apuntan a una aplicación determinada, identificada por un [**ProductCode**](productcode.md), y no deben compartirse entre aplicaciones. Los métodos abreviados anunciados solo funcionan en la aplicación instalada más recientemente y se quitan cuando se quita la aplicación.

Se hace referencia a esta tabla cuando se ejecuta la acción [CreateShortcuts](createshortcuts-action.md) y la [acción RemoveShortcuts](removeshortcuts-action.md) .

Vea también la propiedad [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



