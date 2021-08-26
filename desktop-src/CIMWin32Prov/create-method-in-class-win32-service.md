---
description: 'Método Create de la clase Win32_Service (proveedores WMI CIMWin32): crea un nuevo servicio del sistema.'
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Método Create de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3baa83179ac6c5040aa85a5fcf2af0d932a4c8e9cdc2d10742c5c8aaa66abb5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003805"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método Create de la clase Win32_Service (proveedores WMI CIMWin32)

El **método de** clase Create [WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo servicio del sistema.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Nombre del servicio que se instalará en el **método Create.** La longitud máxima de la cadena es de 256 caracteres. La base de datos de Service Control Manager conserva las mayúsculas y minúsculas de los caracteres, pero las comparaciones de nombres de servicio siempre no tienen en cuenta las mayúsculas y minúsculas. Las barras diagonales (/) y las dos barras diagonales () son \\ caracteres de nombre de servicio no válidos.

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

Controlador recognizer

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

Gravedad del error si el **método Create** no se puede iniciar. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

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

El sistema intenta comenzar con una buena configuración.

</dd> </dl> </dd> <dt>

*StartMode* \[ En\]
</dt> <dd>

Modo de inicio del servicio Windows base.

<dt>

Arranque
</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

Sistema
</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

Automático
</dt> <dd>

Servicio que el Administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

Manual
</dt> <dd>

Servicio que va a iniciar el Administrador de control de servicios cuando un proceso llama al [**método StartService.**](startservice-method-in-class-win32-service.md)

</dd> <dt>

Disabled
</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ En\]
</dt> <dd>

Si **es true,** el servicio puede crear o comunicarse con ventanas en el escritorio.

</dd> <dt>

*StartName* \[ En\]
</dt> <dd>

Nombre de cuenta con el que se ejecuta el servicio. Según el tipo de servicio, el nombre de la cuenta puede tener el formato nombredeusuario de nombre de dominio o nombre principal de \\ usuario (UPN) ( Username@DomainName ). El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica **NULL,** el servicio se inicia sesión como la cuenta LocalSystem. Para un kernel o controladores de nivel de sistema, *StartName* contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio. Ejemplo: Administrador de \\ DWDOM.

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

Matriz que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. Cada elemento de la matriz está delimitado por **NULL** y la lista finaliza con dos **valores NULL.** En Visual Basic o script puede pasar una vbArray. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad **State** de la clase [**\_ BaseService de Win32)**](win32-baseservice.md) es igual a 0, 1 o 2.

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

No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.

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

Se ha quitado del sistema una dependencia en la que se basa este servicio.

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

El servicio tiene dependencias circulares cuando se inicia.

</dd> <dt>

**19**
</dt> <dd>

Un servicio se ejecuta con el mismo nombre.

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

La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Por lo general, los servicios se instalan de una de estas dos maneras: ya sea como parte de la instalación del sistema operativo o mediante un programa de instalación proporcionado por el desarrollador del servicio. Sin embargo, es posible que algunos servicios, especialmente los creados de forma local, no tengan un programa de instalación. En esos casos, puede usar el **método Create** para instalar servicios mediante programación.

A pesar del nombre, el método Create no crea realmente un servicio; simplemente instala un servicio existente. Para usar este comando, debe copiar el archivo ejecutable del servicio en un equipo y, a continuación, usar **Crear** para instalar el servicio.

El **método Create** es similar al método [**Change.**](change-method-in-class-win32-service.md) En ambos casos, las propiedades del servicio se pasan como parámetros al método . Al igual que con los parámetros usados con **el método Change,** el orden en que se pasan estos parámetros es muy importante.

El *parámetro LoadOrderGroup* representa una agrupación de servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.

## <a name="examples"></a>Ejemplos

El siguiente VBScript instala un servicio denominado DbService


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Servicio \_ Win32**](win32-service.md)
</dt> <dt>

[Tareas wmi: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

