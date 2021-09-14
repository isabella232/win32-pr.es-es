---
description: La tabla ServiceInstall se usa para instalar un servicio y tiene las columnas siguientes.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: ServiceInstall Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260900"
---
# <a name="serviceinstall-table"></a>ServiceInstall Table

La tabla ServiceInstall se usa para instalar un servicio y tiene las columnas siguientes.



| Columna         | Tipo                               | Clave | Nullable |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [Identificador](identifier.md)       | Y   | N        |
| Nombre           | [Formato](formatted.md)         | N   | N        |
| DisplayName    | [Formato](formatted.md)         | N   | Y        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Formato](formatted.md)         | N   | Y        |
| Dependencias   | [Formato](formatted.md)         | N   | Y        |
| Startname      | [Formato](formatted.md)         | N   | Y        |
| Contraseña       | [Formato](formatted.md)         | N   | Y        |
| Argumentos      | [Formato](formatted.md)         | N   | Y        |
| Componente\_    | [Identificador](identifier.md)       | N   | N        |
| Descripción    | [Formato](formatted.md)         | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

Esta es la clave principal de la tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Esta columna es la cadena que proporciona el nombre del servicio que se va a instalar. La cadena tiene una longitud máxima de 256 caracteres. La base de datos del administrador de control de servicios conserva las mayúsculas y minúsculas de los caracteres del nombre del servicio, pero las comparaciones de nombres de servicio no tienen en cuenta las mayúsculas y minúsculas. La barra diagonal (/) y la barra diagonal \\ () son caracteres de nombre de servicio no válidos.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Esta columna es la cadena localizable que usan los programas de interfaz de usuario para identificar el servicio. La cadena tiene una longitud máxima de 256 caracteres. El administrador de control de servicios conserva las mayúsculas y minúsculas del nombre para mostrar, pero las comparaciones de nombres para mostrar no tienen en cuenta las mayúsculas y minúsculas.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

Esta columna es un conjunto de marcas de bits que especifican el tipo de servicio. En esta columna se debe especificar uno de los siguientes tipos de servicio.



| Tipo de servicio                | Value      | Descripción                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROCESO \_ PROPIO DE WIN32 \_ DE \_ SERVICIO   | 0x00000010 | Un servicio De Microsoft Win32 que ejecuta su propio proceso.                                                                                                                                                                         |
| PROCESO DE \_ RECURSO COMPARTIDO WIN32 \_ DEL \_ SERVICIO | 0x00000020 | Un servicio Win32 que comparte un proceso.                                                                                                                                                                                       |
| PROCESO \_ INTERACTIVO DE \_ SERVICIO  | 0x00000100 | Un servicio Win32 que interactúa con el escritorio. Este valor no se puede usar por sí solo y debe agregarse a uno de los dos tipos anteriores. La columna StartName debe establecerse en LocalSystem o null cuando se usa esta marca.<br/> |



 

No se admiten los siguientes tipos de servicio.



| Tipo de servicio               | Value      | Descripción                   |
|-------------------------------|------------|-------------------------------|
| CONTROLADOR \_ DE KERNEL DE \_ SERVICIO       | 0x00000001 | Un servicio de controlador.             |
| CONTROLADOR \_ DEL SISTEMA DE ARCHIVOS DE \_ \_ SERVICIO | 0x00000002 | Un servicio de controlador del sistema de archivos. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Esta columna es un conjunto de marcas de bits que especifican cuándo iniciar el servicio. En esta columna se debe especificar uno de los siguientes tipos de inicio de servicio.



| Tipo de inicio de servicio  | Value      | Descripción                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| INICIO \_ AUTOMÁTICO DEL \_ SERVICIO   | 0x00000002 | Un servicio se inicia durante el inicio del sistema.                                                              |
| INICIO DE \_ LA DEMANDA \_ DE SERVICIO | 0x00000003 | Un servicio se inicia cuando el administrador de control de servicios llama a [**la función StartService.**](/windows/win32/api/winsvc/nf-winsvc-startservicea) |
| SERVICIO \_ DESHABILITADO      | 0x00000004 | Especifica un servicio que ya no se puede iniciar.                                                         |



 

El Windows no puede usar las opciones INICIO \_ DE ARRANQUE DEL SERVICIO y INICIO DEL SISTEMA DE \_ \_ \_ SERVICIO.

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Esta columna especifica la acción realizada por el programa de inicio si el servicio no se puede iniciar durante el inicio. Estos valores afectan a los eventos ServiceControl StartService para los servicios instalados. En esta columna se debe especificar una de las siguientes marcas de control de errores.

Al agregar la **constante msidbServiceInstallErrorControlVital** (valor = 0x08000) a las marcas de la tabla siguiente se especifica que se debe producir un error en la instalación general si el servicio no se puede instalar en el sistema.



| Marca de control de error       | Value      | Acción del programa de inicio                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ DE SERVICIO \_ OMITIR   | 0x00000000 | Registra el error y continúa con la operación de inicio.                                                                                                                                       |
| ERROR \_ DE SERVICIO \_ NORMAL   | 0x00000001 | Registra el error, muestra un cuadro de mensaje y continúa la operación de inicio.                                                                                                                    |
| ERROR \_ CRÍTICO DEL \_ SERVICIO | 0x00000003 | Registra el error si es posible y el sistema se reinicia con la última configuración que se sabe que es buena. Si se está iniciando la última configuración correcta conocida, se produce un error en la operación de inicio. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Esta columna contiene la cadena que denomina al grupo de ordenación de carga del que es miembro este servicio. Especifique null o una cadena vacía si el servicio no pertenece a un grupo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependencias
</dt> <dd>

Esta columna es una lista de nombres de servicios o grupos de ordenación de carga que el sistema debe iniciar antes de este servicio. Separe los nombres de la lista por Valores NULL. Si el servicio no tiene dependencias, especifique Null o una cadena vacía. Use la \[ ~ \] sintaxis para insertar un valor NULL. La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.

Por ejemplo, para requerir que el sistema inicie service1 y service2, antes de iniciar el servicio que aparece en la columna ServiceInstall , escriba service1 service2 en la \[ ~ \] \[ ~ \] \[ ~ \] columna Dependencias. Los identificadores service1 y service2 deben aparecer en la clave principal de la tabla o ser el nombre del servicio que ya está instalado.

Debe antecedido los nombres de grupo con + para que se puedan distinguir de un nombre de servicio. Para requerir que el sistema inicie service1 y al menos un miembro del grupo de pedidos MyGroup antes de iniciar el servicio enumerado en la columna ServiceInstall , escriba service1 \[ ~ \] +MyGroup \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>Startname
</dt> <dd>

El servicio se inicia sesión como el nombre especificado por la cadena de esta columna. Si el tipo de servicio es SERVICE \_ WIN32 OWN PROCESS, use un \_ nombre de cuenta con el \_ formato: NombreDeServidor \\ NombreDe DomainName. Si la cuenta pertenece al dominio integrado, se permite especificar . \\ Nombre de usuario. La cuenta LocalSystem debe usarse si el tipo de servicio es SERVICE \_ WIN32 \_ SHARE PROCESS o SERVICE INTERACTIVE \_ \_ \_ PROCESS. La [**función CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usa la cuenta LocalSystem si StartName se especifica como null y, por tanto, la mayoría de los servicios dejan esta columna en blanco.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Contraseña
</dt> <dd>

Esta cadena es la contraseña del nombre de cuenta especificado en la columna StartName. Tenga en cuenta que el usuario debe tener permisos para iniciar sesión como servicio. El servicio no tiene contraseña si StartName es null o una cadena vacía. Startname de LocalSystem es NULL y, por tanto, la contraseña de esta instancia es NULL, por lo que la mayoría de los servicios dejan esta columna en blanco.

Tenga en cuenta que después de eliminar un servicio que se instaló con un nombre de usuario y una contraseña, el instalador no puede revertir el servicio sin usar primero una acción personalizada para obtener la contraseña. El instalador puede adquirir toda la información necesaria sobre el servicio, excepto la contraseña, que se almacena en una parte protegida del sistema. La acción personalizada adquiere la contraseña solicitando al usuario, leyendo una propiedad de la base de datos o leyendo un archivo. A continuación, la acción personalizada debe [**llamar a ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)para proporcionar la contraseña, antes de volver a instalar el servicio.

Windows El instalador no escribe el valor especificado en el campo Contraseña en el archivo de registro.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Esta columna contiene los argumentos o propiedades de la línea de comandos necesarios para ejecutar el servicio.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa para la columna uno de la [tabla de componentes](component-table.md). Tenga en cuenta que para instalar este servicio mediante la tabla InstallService, keyPath para este componente debe ser el archivo ejecutable para el servicio.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Esta columna contiene una descripción localizable para el servicio que se está configurando. Si esta columna se deja en blanco, el instalador usa la descripción existente del servicio si existe alguna. Para obtener más información, vea DESCRIPCIÓN \_ DEL SERVICIO en Microsoft Windows Software Development Kit (SDK). Para borrar una descripción existente, escriba " \[ ~ \] " en esta columna. Esto da como resultado una descripción en blanco para un servicio nuevo o existente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción InstallServices](installservices-action.md) de [*las tablas de secuencia*](s-gly.md) procesa la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

Esta tabla tiene la mayoría de los parámetros de la función [**CreateService de**](/windows/win32/api/winsvc/nf-winsvc-createservicea) Win32.

Aunque es posible usar la interfaz de usuario para especificar que un servicio se instale como run-from-source, el instalador no admite realmente este tipo de instalación. Los servicios que se ejecutan con el nivel de privilegio del sistema local deben instalarse para ejecutarse desde el disco duro local. Evite instalar servicios que suplante los privilegios de un usuario determinado, ya que esto puede escribir datos de seguridad en un registro o en el registro del sistema. Esto puede crear un problema de seguridad, un conflicto de contraseñas o la pérdida de datos de configuración cuando se reinicia el sistema.

Para eliminar un servicio durante una desinstalación, debe haber un registro correspondiente para el servicio en la tabla [ServiceControl](servicecontrol-table.md) y la marca **msidbServiceControlEventUninstallDelete** debe aparecer en la columna Evento. El instalador no elimina un servicio de la tabla ServiceInstall durante la desinstalación sin esta entrada en la tabla ServiceControl.

Para obtener información sobre cómo proteger un servicio, vea [la tabla MsiLockPermissionsEx](msilockpermissionsex-table.md).

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

 

 
