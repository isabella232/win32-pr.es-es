---
title: Método Create de la clase Win32_Service (Servicios de Escritorio remoto)
description: Crea un nuevo servicio de sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_Service (clase)
- Win32_Service Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44d6c67e0d5bd6333f57c44cc44c25dc64e04a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491602"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a>Método Create de la clase Win32_Service (Servicios de Escritorio remoto)

El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio de sistema.

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

Nombre del servicio que se va a instalar en el método **Create** . La longitud de cadena máxima es de 256 caracteres. La base de datos del administrador de control de servicios conserva el uso de mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio no distinguen mayúsculas de minúsculas. Barras diagonales (/) y dobles barras diagonales (los \) caracteres de nombre de servicio no son válidos).

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

Gravedad del error si el método **Create** no se inicia. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

0
</dt> <dd>

No se notifica al usuario.

</dd> <dt>

1
</dt> <dd>

Se notifica al usuario.

</dd> <dt>

2
</dt> <dd>

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

3
</dt> <dd>

El sistema intenta iniciarse con una configuración válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ de\]
</dt> <dd>

Modo de inicio del servicio base de Windows.

<dt>

Arranque
</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

System
</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

Automático
</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

Manual
</dt> <dd>

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](win32-terminalservice-startservice.md) .

</dd> <dt>

Disabled
</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ de\]
</dt> <dd>

Si **es true**, el servicio puede crear o comunicarse con Windows en el escritorio.

</dd> <dt>

*StartName* \[ de\]
</dt> <dd>

Nombre de cuenta con la que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de cuenta puede tener el \\ formato nombrededominio nombredeusuario o nombre principal de usuario (UPN) ( Username@DomainName ). El proceso de servicio se registra con una de estas dos formas cuando se ejecuta. Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario. Si se especifica **null** , el servicio inicia sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo. Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio. Ejemplo: DWDOM \\ admin.

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

Matriz de que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. Cada elemento de la matriz está delimitado por **null** y la lista termina en dos valores **null** . En Visual Basic o script puede pasar un objeto vbArray. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Se aceptó la solicitud.

</dd> <dt>

**1**
</dt> <dd>

No se admite la solicitud.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tenía el acceso necesario.

</dd> <dt>

**3**
</dt> <dd>

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**4**
</dt> <dd>

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**5**
</dt> <dd>

El código de control solicitado no se puede enviar al servicio porque el estado de la propiedad Service (**State** de la clase [**\_ BaseService de Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) es igual a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

El servicio no se ha iniciado.

</dd> <dt>

**7**
</dt> <dd>

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido al iniciar el servicio.

</dd> <dt>

**9**
</dt> <dd>

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**10**
</dt> <dd>

El servicio ya se está ejecutando.

</dd> <dt>

**11**
</dt> <dd>

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**12**
</dt> <dd>

Una dependencia de la que depende este servicio se ha quitado del sistema.

</dd> <dt>

**13**
</dt> <dd>

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**14**
</dt> <dd>

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**15**
</dt> <dd>

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**16**
</dt> <dd>

Este servicio se está quitando del sistema.

</dd> <dt>

**17**
</dt> <dd>

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>

**18**
</dt> <dd>

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>

**19**
</dt> <dd>

Se está ejecutando un servicio con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**21**
</dt> <dd>

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, los servicios se instalan de una de estas dos maneras: como parte de la instalación del sistema operativo o mediante un programa de instalación proporcionado por el desarrollador del servicio. Sin embargo, es posible que algunos servicios, especialmente los creados internamente, no tengan un programa de instalación. En esos casos, puede utilizar el método **Create** para instalar los servicios mediante programación.

A pesar del nombre, el método Create no crea un servicio en realidad. simplemente instala un servicio existente. Para usar este comando, debe copiar el archivo ejecutable del servicio en un equipo y, a continuación, usar **crear** para instalar el servicio.

El método **Create** es similar al método [**Change**](win32-terminalservice-change.md) . En ambos casos, las propiedades del servicio se pasan como parámetros al método. Al igual que con los parámetros que se usan con el método **Change** , el orden en el que se pasan estos parámetros es muy importante.

El parámetro *LoadOrderGroup* representa una agrupación de los servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Tareas WMI: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

