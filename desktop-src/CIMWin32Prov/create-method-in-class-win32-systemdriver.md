---
description: Crea un nuevo servicio administrado por el controlador del sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Método Create de la clase Win32_SystemDriver
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153569"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Método Create de la \_ clase Win32 SystemDriver

El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio administrado por el controlador del sistema. El *parámetro \_ LoadOrderGroup de Win32* representa una agrupación de los servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*Nombre* \[ de de\]
</dt> <dd>

Nombre del servicio que se va a instalar en el método **Create** . La longitud de cadena máxima es de 256 caracteres. La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas. Las barras diagonales (/) y dos barras diagonales inversas ( \\ ) son caracteres de nombre de servicio no válidos.

</dd> <dt>

*DisplayName* \[ de\]
</dt> <dd>

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios. Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.

Constraints: acepta el mismo valor que el parámetro *Name* .

Ejemplo: "Endisco".

</dd> <dt>

*Nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio.

Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ de\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

1 (0x1)
</dt> <dd>

Controlador de kernel

</dd> <dt>

2 (0X2)
</dt> <dd>

Controlador del sistema de archivos

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter (Adaptador)

</dd> <dt>

8 (0x8)
</dt> <dd>

Controlador del reconocedor

</dd> <dt>

16 (0x10)
</dt> <dd>

Proceso propio

</dd> <dt>

32 (0x20)
</dt> <dd>

Compartir proceso

</dd> <dt>

256 (0x100)
</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ de\]
</dt> <dd>

Gravedad del error si el método **Create** no se inicia. Este valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

0
</dt> <dd>

Omitir

No se notifica al usuario.

</dd> <dt>

1
</dt> <dd>

"Normal"

Se notifica al usuario.

</dd> <dt>

2
</dt> <dd>

Fuertes

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

3
</dt> <dd>

Suma

El sistema intenta iniciarse con una configuración válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ de\]
</dt> <dd>

Modo de inicio del servicio base de Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**


</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Integrado**


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**


</dt> <dd>

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**


</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ de\]
</dt> <dd>

Si **es true**, el servicio puede crear o comunicarse con las ventanas del escritorio.

</dd> <dt>

*StartName* \[ de\]
</dt> <dd>

Nombre de cuenta con la que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de cuenta puede tener el \\ formato nombrededominio nombredeusuario o nombre principal de usuario (UPN) ( Username@DomainName ). El proceso de servicio se registra con una de estas dos formas cuando se ejecuta. Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario. Si se especifica **null** , el servicio inicia sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo. Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.

Ejemplo: DWDOM \\ admin

</dd> <dt>

*StartPassword* \[ de\]
</dt> <dd>

Contraseña para el nombre de cuenta especificado por el parámetro *StartName* . Especifique **null** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

</dd> <dt>

*LoadOrderGroup* \[ de\]
</dt> <dd>

Nombre de grupo asociado al nuevo servicio. Los grupos de pedidos de carga se incluyen en el registro y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **null** o apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* . Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo. El registro tiene una lista de grupos de orden de carga que se encuentran en:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ de\]
</dt> <dd>

Matriz de grupos de orden de carga que deben iniciarse antes de este servicio. Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** . En Visual Basic o script puede pasar un objeto vbArray. Si el puntero es **null** o apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlo de un nombre de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ de\]
</dt> <dd>

Una matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** . En Visual Basic o script puede pasar un objeto vbArray. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se creó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

