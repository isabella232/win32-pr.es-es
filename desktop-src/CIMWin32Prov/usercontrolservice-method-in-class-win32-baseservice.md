---
description: Intenta enviar un código de control definido por el usuario a un servicio.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907465"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>Método UserControlService de la \_ clase BaseService de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) intenta enviar un código de control definido por el usuario a un servicio.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ControlCode* \[ de\]
</dt> <dd>

Valor que especifica un comando de control para un servicio. Por ejemplo, un comando de control es un comando de "pausa" o "continuar". El valor puede ser un código predefinido, o un valor y una acción que define el servicio. Estos son los códigos de control predefinidos:

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_continuar con el control de servicio \_**


</dt> <dd>

Notifica a un servicio en pausa que se reanude.

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_interrogación de control de servicio \_**


</dt> <dd>

Notifica a un servicio que informe de la información de estado actual al administrador de control de servicios.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de control de servicio \_**


</dt> <dd>

Notifica a un servicio de red que hay un nuevo componente para el enlace.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de control de servicio \_**


</dt> <dd>

Notifica a un servicio de red que uno de sus enlaces está deshabilitado.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de control de servicio \_**


</dt> <dd>

Notifica a un servicio de red que se ha habilitado un enlace deshabilitado.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de control de servicio \_**


</dt> <dd>

Notifica a un servicio de red que se ha quitado un componente para el enlace.

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de control de servicio \_**


</dt> <dd>

Notifica a un servicio que se han modificado sus parámetros de inicio.

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_pausa de control de servicio \_**


</dt> <dd>

Notifica a un servicio que se PAUSE.

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_detención del control de servicio \_**


</dt> <dd>

Notifica a un servicio que se detenga.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Se acepta la solicitud.

</dd> <dt>

**No compatible**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tiene los derechos de acceso necesarios.

</dd> <dt>

**Servicios dependientes en ejecución**
</dt> <dd>

3

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**Control de servicio no válido**
</dt> <dd>

4

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**El servicio no puede aceptar el control**
</dt> <dd>

5

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.

</dd> <dt>

**Servicio no activo**
</dt> <dd>

6

No se inició el servicio.

</dd> <dt>

**Tiempo de espera de solicitud de servicio**
</dt> <dd>

7

El servicio no responde rápidamente a la solicitud de inicio.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Proceso interactivo.

</dd> <dt>

**Ruta de acceso no encontrada**
</dt> <dd>

9

No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**El servicio ya se está ejecutando**
</dt> <dd>

10

El servicio ya se está ejecutando.

</dd> <dt>

**Base de datos de servicio bloqueada**
</dt> <dd>

11

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**Dependencia de servicio eliminada**
</dt> <dd>

12

Una dependencia en la que se basa este servicio se quita del sistema.

</dd> <dt>

**Error de dependencia de servicio**
</dt> <dd>

13

El servicio no encuentra el servicio necesario de un servicio dependiente.

</dd> <dt>

**Servicio deshabilitado**
</dt> <dd>

14

El servicio está deshabilitado del sistema.

</dd> <dt>

**Error de inicio de sesión de servicio**
</dt> <dd>

15

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**Servicio marcado para eliminación**
</dt> <dd>

16

El servicio se va a quitar del sistema.

</dd> <dt>

**Servicio sin subproceso**
</dt> <dd>

17

No hay ningún subproceso de ejecución para el servicio.

</dd> <dt>

**Estado dependencia circular**
</dt> <dd>

18

Hay dependencias circulares al iniciarse el servicio.

</dd> <dt>

**Estado nombre duplicado**
</dt> <dd>

19

Hay un servicio que se ejecuta con el mismo nombre.

</dd> <dt>

**Estado nombre no válido**
</dt> <dd>

20

Hay caracteres no válidos en el nombre del servicio.

</dd> <dt>

**Estado parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Estado cuenta de servicio no válida**
</dt> <dd>

22

La cuenta con la que se ejecuta este servicio no es válida o no tiene permisos para ejecutar el servicio.

</dd> <dt>

**El servicio de estado existe**
</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**Servicio ya pausado**
</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

25 4294967295

</dd> </dl>

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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

