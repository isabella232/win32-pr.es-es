---
description: La tabla ServiceInstall se utiliza para instalar un servicio y tiene las columnas siguientes.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabla ServiceInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667749"
---
# <a name="serviceinstall-table"></a>Tabla ServiceInstall

La tabla ServiceInstall se utiliza para instalar un servicio y tiene las columnas siguientes.



| Columna         | Tipo                               | Clave | Nullable |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [Identificador](identifier.md)       | Y   | N        |
| Nombre           | [Formatea](formatted.md)         | N   | N        |
| DisplayName    | [Formatea](formatted.md)         | N   | Y        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Formatea](formatted.md)         | N   | Y        |
| Dependencias   | [Formatea](formatted.md)         | N   | Y        |
| StartName      | [Formatea](formatted.md)         | N   | Y        |
| Contraseña       | [Formatea](formatted.md)         | N   | Y        |
| Argumentos      | [Formatea](formatted.md)         | N   | Y        |
| Componente\_    | [Identificador](identifier.md)       | N   | N        |
| Descripción    | [Formatea](formatted.md)         | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

Esta es la clave principal de la tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Esta columna es la cadena que proporciona el nombre del servicio que se va a instalar. La cadena tiene una longitud máxima de 256 caracteres. La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas en los caracteres del nombre del servicio, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas. La barra diagonal (/) y la barra diagonal inversa ( \\ ) son caracteres de nombre de servicio no válidos.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Mostrar
</dt> <dd>

Esta columna es la cadena localizable que los programas de la interfaz de usuario usan para identificar el servicio. La cadena tiene una longitud máxima de 256 caracteres. El administrador de control de servicios conserva las mayúsculas y minúsculas del nombre para mostrar, pero las comparaciones de nombres para mostrar no distinguen mayúsculas de minúsculas.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

Esta columna es un conjunto de marcadores de bits que especifican el tipo de servicio. En esta columna se debe especificar uno de los siguientes tipos de servicio.



| Tipo de servicio                | Value      | Descripción                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Proceso propio del servicio Win32 \_   | 0x00000010 | Un servicio de Microsoft Win32 que ejecuta su propio proceso.                                                                                                                                                                         |
| \_Proceso de \_ recurso compartido de Win32 de servicio \_ | 0x00000020 | Servicio de Win32 que comparte un proceso.                                                                                                                                                                                       |
| \_proceso interactivo de servicio \_  | 0x00000100 | Servicio de Win32 que interactúa con el escritorio. Este valor no se puede usar por sí solo y debe agregarse a uno de los dos tipos anteriores. La columna StartName debe establecerse en LocalSystem o null al usar esta marca.<br/> |



 

No se admiten los siguientes tipos de servicio.



| Tipo de servicio               | Value      | Descripción                   |
|-------------------------------|------------|-------------------------------|
| \_controlador de kernel de servicio \_       | 0x00000001 | Un servicio de controlador.             |
| \_ \_ controlador del sistema de archivos del servicio \_ | 0x00000002 | Un servicio de controlador del sistema de archivos. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Esta columna es un conjunto de marcas de bits que especifican Cuándo se debe iniciar el servicio. En esta columna se debe especificar uno de los siguientes tipos de inicio del servicio.



| Tipo de inicio de servicio  | Value      | Descripción                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| \_Inicio automático del servicio \_   | 0x00000002 | Se inicia un servicio durante el inicio del sistema.                                                              |
| Inicio de la demanda de servicio \_ \_ | 0x00000003 | Un servicio se inicia cuando el administrador de control de servicios llama a la función [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) . |
| SERVICIO \_ deshabilitado      | 0x00000004 | Especifica un servicio que ya no se puede iniciar.                                                         |



 

El Windows Installer no puede usar las \_ Opciones de inicio \_ del sistema de inicio y de inicio \_ del servicio \_ .

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Esta columna especifica la acción realizada por el programa de inicio si el servicio no se inicia durante el inicio. Estos valores afectan a los eventos de ServiceControl StartService para los servicios instalados. Se debe especificar una de las siguientes marcas de control de errores en esta columna.

Al agregar la constante **msidbServiceInstallErrorControlVital** (Value = 0x08000) a las marcas de la tabla siguiente, se especifica que se debe producir un error en la instalación general si el servicio no se puede instalar en el sistema.



| Marca de control de errores       | Value      | Acción del programa de inicio                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_omitir error de servicio \_   | 0x00000000 | Registra el error y continúa con la operación de inicio.                                                                                                                                       |
| ERROR de servicio \_ \_ normal   | 0x00000001 | Registra el error, muestra un cuadro de mensaje y continúa con la operación de inicio.                                                                                                                    |
| ERROR de servicio \_ \_ crítico | 0x00000003 | Registra el error si es posible y el sistema se reinicia con la última configuración que se sabe que es correcta. Si se está iniciando la última configuración válida conocida, se produce un error en la operación de inicio. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Esta columna contiene la cadena que nombra el grupo de pedidos de carga del que es miembro este servicio. Especifique NULL o una cadena vacía si el servicio no pertenece a un grupo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependencias
</dt> <dd>

Esta columna es una lista de nombres de servicios o grupos de orden de carga que el sistema debe iniciar antes de este servicio. Separe los nombres de la lista por valores NULL. Si el servicio no tiene dependencias, especifique NULL o una cadena vacía. Use la sintaxis \[ ~ \] para insertar un valor null. La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.

Por ejemplo, para requerir que el sistema inicie Service1 y service2, antes de iniciar el servicio que se muestra en la columna ServiceInstall, escriba Service1 \[ ~ \] service2 \[ ~ \] \[ ~ \] en la columna dependencies. Los identificadores Service1 y service2 deben aparecer en la clave principal de la tabla o ser el nombre del servicio que ya está instalado.

Debe prefijar los nombres de grupo con + para que se puedan distinguir de un nombre de servicio. Para requerir que el sistema inicie Service1 y al menos un miembro del grupo de pedidos, antes de iniciar el servicio que se muestra en la columna ServiceInstall, escriba Service1 \[ ~ \] + mi grupo \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

El servicio ha iniciado sesión como el nombre dado por la cadena en esta columna. Si el tipo de servicio es \_ servicio \_ propio \_ de Win32, use un nombre de cuenta con el formato: nombrededominio \\ nombreDeUsuario. Si la cuenta pertenece al dominio integrado, se le permite especificar. \\ Nombre. Se debe usar la cuenta LocalSystem si el tipo de servicio es servicio \_ de \_ recursos compartidos de Win32 \_ o \_ proceso interactivo de servicio \_ . La función [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usa la cuenta LocalSystem si StartName se especifica como NULL y la mayoría de los servicios deja esta columna en blanco.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Contraseña
</dt> <dd>

Esta cadena es la contraseña del nombre de cuenta especificado en la columna StartName. Tenga en cuenta que el usuario debe tener permisos para iniciar sesión como servicio. El servicio no tiene contraseña si StartName es null o una cadena vacía. La StartName de LocalSystem es NULL y, por lo tanto, la contraseña de esta instancia es null, por lo que la mayoría de los servicios deja esta columna en blanco.

Tenga en cuenta que, después de eliminar un servicio que se instaló con un nombre de usuario y una contraseña, el instalador no puede revertir el servicio sin usar primero una acción personalizada para obtener la contraseña. El instalador puede adquirir toda la información necesaria sobre el servicio, excepto la contraseña, que se almacena en una parte protegida del sistema. La acción personalizada adquiere la contraseña solicitando al usuario, leyendo una propiedad de la base de datos o leyendo un archivo. La acción personalizada debe llamar a [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)para proporcionar la contraseña antes de volver a instalar el servicio.

Windows Installer no escribe el valor especificado en el campo de contraseña en el archivo de registro.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Esta columna contiene los argumentos de la línea de comandos o las propiedades necesarias para ejecutar el servicio.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa para la columna uno de la [tabla de componentes](component-table.md). Tenga en cuenta que para instalar este servicio mediante la tabla InstallService, la ruta de acceso de este componente debe ser el archivo ejecutable del servicio.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Esta columna contiene una descripción localizable para el servicio que se está configurando. Si esta columna se deja en blanco, el instalador usa la descripción existente del servicio si existe una. Para obtener más información, vea \_ Descripción del servicio en el kit de desarrollo de software (SDK) de Microsoft Windows. Para borrar una descripción existente, escriba " \[ ~ \] " en esta columna. Esto da como resultado una descripción en blanco para un servicio nuevo o existente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La acción [InstallServices](installservices-action.md) de [*las tablas de secuencia*](s-gly.md) procesa la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

Esta tabla tiene la mayoría de los parámetros de la función de Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) .

Aunque es posible usar la interfaz de usuario para especificar que un servicio se instale como ejecutar desde el origen, el instalador no es compatible realmente con este tipo de instalación. Los servicios que se ejecutan con el nivel de privilegios del sistema local deben estar instalados para ejecutarse desde la unidad de disco duro local. Evite la instalación de servicios que suplanten los privilegios de un usuario determinado, ya que esto puede escribir datos de seguridad en un registro o en el registro del sistema. Esto puede crear un problema de seguridad, un conflicto de contraseña o la pérdida de datos de configuración cuando se reinicia el sistema.

Para eliminar un servicio durante una desinstalación, debe haber un registro correspondiente para el servicio en la [tabla ServiceControl](servicecontrol-table.md) y la marca **msidbServiceControlEventUninstallDelete** debe aparecer en la columna Event. El instalador no elimina un servicio de la tabla ServiceInstall durante la desinstalación sin esta entrada en la tabla ServiceControl.

Para obtener información sobre cómo proteger un servicio, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
