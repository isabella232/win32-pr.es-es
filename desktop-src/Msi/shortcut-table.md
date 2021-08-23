---
description: La tabla Acceso directo contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabla de métodos abreviados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628425"
---
# <a name="shortcut-table"></a>Tabla de métodos abreviados

La tabla Acceso directo contiene la información que la aplicación necesita para crear accesos directos en el equipo del usuario.

La tabla Acceso directo tiene las siguientes columnas.



| Columna                 | Tipo                         | Clave | Nullable |
|------------------------|------------------------------|-----|----------|
| Acceso directo               | [Identificador](identifier.md) | Y   | N        |
| Directorio\_            | [Identificador](identifier.md) | N   | N        |
| Nombre                   | [Nombre de archivo](filename.md)     | N   | N        |
| Componente\_            | [Identificador](identifier.md) | N   | N        |
| Destino                 | [Acceso directo](shortcut.md)     | N   | N        |
| Argumentos              | [Formato](formatted.md)   | N   | Y        |
| Descripción            | [Texto](text.md)             | N   | Y        |
| Tecla de acceso rápido                 | [Entero](integer.md)       | N   | Y        |
| Icono\_                 | [Identificador](identifier.md) | N   | Y        |
| IconIndex              | [Entero](integer.md)       | N   | Y        |
| ShowCmd                | [Entero](integer.md)       | N   | Y        |
| WkDir                  | [Identificador](identifier.md) | N   | Y        |
| DisplayResourceDLL     | [Formato](formatted.md)   | N   | Y        |
| DisplayResourceId      | [Entero](integer.md)       | N   | Y        |
| DescriptionResourceDLL | [Formato](formatted.md)   | N   | Y        |
| DescriptionResourceId  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Acceso directo
</dt> <dd>

Valor de clave de esta tabla.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directorio\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Directory](directory-table.md). Esta columna especifica el directorio en el que se crea el archivo de acceso directo.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre localizable del acceso directo que se va a crear.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md). El instalador usa el estado de instalación del componente especificado en esta columna para determinar si se crea o elimina el acceso directo. Este componente debe tener una ruta de acceso de clave válida para que se instale el acceso directo. Si la columna Destino contiene el nombre de una característica, el archivo iniciado por el acceso directo es el archivo clave del componente enumerado en esta columna.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Objetivo
</dt> <dd>

Destino del acceso directo.

Para un acceso directo anunciado, esta columna debe ser una clave externa en la primera columna de la [tabla Feature](feature-table.md). El instalador evalúa la entrada del [](identifier.md) campo Destino como identificador y la entrada debe ser una clave externa válida en la [tabla de características](feature-table.md). El archivo iniciado por el acceso directo en este caso es el archivo clave del componente enumerado en la columna \_ Componente . Cuando se activa el acceso directo, el instalador comprueba que todos los componentes de la característica están instalados antes de iniciar este archivo.

Para un acceso directo no anunciado, el instalador evalúa este campo como una [cadena con](formatted.md) formato. El campo debe incluir un identificador de propiedad entre corchetes ( ), que se expande en el archivo o en una carpeta a la que apunta \[ \] el acceso directo. Para obtener más información, vea la [acción CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Argumentos de la línea de comandos para el acceso directo.

Tenga en cuenta que la resolución de propiedades en el campo Argumentos es limitada. Una propiedad con formato Propiedad en este campo solo se puede resolver si la propiedad ya tiene el valor previsto cuando se instala el componente propietario \[  \] del acceso directo. Por ejemplo, para resolver en el valor correcto para el argumento "MyDoc.doc", el mismo proceso debe instalar el archivo MyDoc.doc y el componente que posee el acceso \[ \# \] directo.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción localizable del acceso directo.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey
</dt> <dd>

Tecla de acceso rápido para el acceso directo. El byte de orden bajo contiene el código de clave virtual de la clave y el byte de orden superior contiene marcas modificadoras. Debe ser un número no negativo. Por lo general, se recomienda que los autores de paquetes de instalación no establezcan esta opción, ya que el valor de esta opción puede agregar teclas de acceso rápido duplicadas al escritorio de un usuario. Además, la práctica de asignar teclas de acceso rápido a accesos directos puede ser problemática para los usuarios que usan teclas de acceso rápido para [la accesibilidad.](accessibility.md)

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

Clave externa para la columna uno de la [tabla Icon](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice de icono del acceso directo. Debe ser un número no negativo.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

El comando Show de la ventana de la aplicación.

Se pueden usar los siguientes valores. Los valores se definen para la función Windows API ShowWindow.



| Valor | Significado             |
|-------|---------------------|
| 1     | SW \_ SHOWNORMAL      |
| 3     | SW \_ SHOWMAXIMIZED   |
| 7     | SW \_ SHOWMINNOACTIVE |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Nombre de la propiedad que tiene la ruta de acceso del directorio de trabajo para el acceso directo. El valor puede usar el formato Windows para hacer referencia a variables de entorno, por ejemplo %USERPROFILE%. Las referencias se resuelven en una ruta de acceso real cuando el instalador resuelve el directorio de trabajo para crear el acceso directo.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Este campo contiene un valor [de](formatted.md) cadena con formato para la ruta de acceso completa al archivo ejecutable portátil con idioma neutro (archivo LN) que contiene los datos de configuración de recursos (RC Config). La cadena con formato puede usar la \[ \# convención \] filekey. Si este campo contiene un valor, se omite la columna Nombre. Si este campo está vacío, el instalador usa el valor de la columna Nombre. Cuando este campo contiene un valor, el **campo DisplayResourceId** también debe contener un valor o se produce un error en la instalación.

Esta columna de la tabla Acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones anteriores a Windows Installer 4.0.

Para obtener información sobre cómo agregar accesos directos a la tabla de accesos directos para su uso con recursos de MUI, vea Ejemplo de [un acceso directo de MUI.](a-mui-shortcut-example.md)

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Índice de nombre para mostrar del acceso directo. Debe ser un número no negativo. Cuando este campo contiene un valor, el **campo DisplayResourceDLL** también debe contener un valor o se produce un error en la instalación.

Esta columna de la tabla Acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones anteriores a Windows Installer 4.0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Este campo contiene un valor [de](formatted.md) cadena con formato para la ruta de acceso completa al archivo ejecutable portátil con idioma neutro (archivo LN) que contiene los datos de configuración de recursos (RC Config). La cadena con formato puede usar la \[ \# convención \] filekey. Si este campo contiene un valor, se omite la columna Nombre. Si este campo está vacío, el instalador usa el valor de la columna Descripción. Cuando este campo contiene un valor, el **campo DescriptionResourceId** también debe contener un valor o se produce un error en la instalación.

Esta columna de la tabla Acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones anteriores a Windows Installer 4.0.

Para obtener información sobre cómo agregar accesos directos a la tabla de accesos directos para su uso con recursos de MUI, vea Ejemplo de [un acceso directo de MUI.](a-mui-shortcut-example.md)

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Índice de nombre de descripción del acceso directo. Debe ser un número no negativo. Cuando este campo contiene un valor, el **campo DescriptionResourceDLL** también debe contener un valor o se produce un error en la instalación.

Esta columna de la tabla Acceso directo solo se usa cuando se ejecuta en Windows Vista o Windows Server 2008 y, de lo contrario, se omite. Esta columna está disponible con versiones anteriores a Windows Installer 4.0.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La habilitación de una característica crea un acceso directo anunciado solo si la interfaz IShellLink del sistema admite la resolución del descriptor del instalador. Esto es compatible con Microsoft Windows 2000 y sistemas que ejecutan Microsoft Internet Explorer 4.01. Si no se admite, el instalador crea un acceso directo no anunciado tras la instalación del componente de la característica, ya sea localmente o desde el origen.

Tenga en cuenta que los accesos directos anunciados siempre apuntan a una aplicación determinada, identificada por [**productCode**](productcode.md), y no deben compartirse entre aplicaciones. Los accesos directos anunciados solo funcionan para la aplicación instalada más recientemente y se quitan cuando se quita esa aplicación.

Se hace referencia a esta tabla cuando se ejecuta [la acción CreateShortcuts](createshortcuts-action.md) y [la acción RemoveShortcuts.](removeshortcuts-action.md)

Vea también la [**propiedad DISABLEADVTSHORTCUTS.**](disableadvtshortcuts.md)

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

 

 



