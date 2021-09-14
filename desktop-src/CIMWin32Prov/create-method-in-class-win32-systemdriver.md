---
description: Crea un nuevo servicio administrado por el controlador del sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Método Create de la Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062730"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Método Create de la clase \_ SystemDriver de Win32

El **método de** clase [Create WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio administrado por el controlador del sistema. El *parámetro \_ LoadOrderGroup de Win32* representa una agrupación de servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del servicio que se instalará en el **método Create.** La longitud máxima de la cadena es de 256 caracteres. La base de datos de Service Control Manager conserva las mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio siempre no tienen en cuenta las mayúsculas y minúsculas. Las barras diagonales (/) y las dos barras diagonales () son caracteres de nombre de \\ servicio no válidos.

</dd> <dt>

*DisplayName* \[ En\]
</dt> <dd>

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en el Administrador de control de servicios. *Las comparaciones* de DisplayName siempre no tienen en cuenta las mayúsculas y minúsculas.

Restricciones: acepta el mismo valor que el *parámetro Name.*

Ejemplo: "Atdisk".

</dd> <dt>

*PathName* \[ En\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio.

Ejemplo: " \\ SystemRoot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ En\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

1 (0x1)
</dt> <dd>

Controlador kernel

</dd> <dt>

2 (0x2)
</dt> <dd>

Controlador del sistema de archivos

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter (Adaptador)

</dd> <dt>

8 (0x8)
</dt> <dd>

Controlador de Recognizer

</dd> <dt>

16 (0x10)
</dt> <dd>

Proceso propio

</dd> <dt>

32 (0x20)
</dt> <dd>

Proceso de recurso compartido

</dd> <dt>

256 (0x100)
</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ En\]
</dt> <dd>

Gravedad del error si el **método Create** no se puede iniciar. Este valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

0
</dt> <dd>

"Omitir"

No se notifica al usuario.

</dd> <dt>

1
</dt> <dd>

"Normal"

Se notifica al usuario.

</dd> <dt>

2
</dt> <dd>

"Grave"

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

3
</dt> <dd>

"Crítico"

El sistema intenta comenzar con una buena configuración.

</dd> </dl> </dd> <dt>

*StartMode* \[ En\]
</dt> <dd>

Modo de inicio del servicio Windows base.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**


</dt> <dd>

Servicio que el Administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**


</dt> <dd>

Servicio que debe iniciar el Administrador de control de servicios cuando un proceso llame al [**método StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado**


</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ En\]
</dt> <dd>

Si **es true,** el servicio puede crear o comunicarse con las ventanas del escritorio.

</dd> <dt>

*StartName* \[ En\]
</dt> <dd>

Nombre de cuenta con el que se ejecuta el servicio. Según el tipo de servicio, el nombre de la cuenta puede tener el formato nombredeusuario de nombre de dominio o nombre principal de \\ usuario (UPN) ( Username@DomainName ). El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica **NULL,** el servicio se inicia sesión como la cuenta LocalSystem. Para un kernel o controladores de nivel de sistema, *StartName* contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S en función del nombre del servicio.

Ejemplo: Administrador \\ de DWDOM

</dd> <dt>

*StartPassword* \[ En\]
</dt> <dd>

Contraseña en el nombre de cuenta especificado por el *parámetro StartName.* Especifique **NULL** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

</dd> <dt>

*LoadOrderGroup* \[ En\]
</dt> <dd>

Nombre de grupo asociado al nuevo servicio. Los grupos de pedidos de carga se encuentran en el Registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el *parámetro LoadOrderGroupDependencies.* Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo. El registro tiene una lista de grupos de ordenación de carga ubicados en:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ En\]
</dt> <dd>

Matriz de grupos de ordenación de carga que deben iniciarse antes de este servicio. Cada elemento de la matriz está delimitado por **NULL** y la lista finaliza con dos **valores NULL.** En Visual Basic o script puede pasar una vbArray. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo Winsvc.h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ En\]
</dt> <dd>

Matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. Cada elemento de la matriz está delimitado por **NULL** y la lista termina con dos **valores NULL.** En Visual Basic o script, puede pasar una vbArray. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se creó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

