---
description: Modifica el modo de inicio de un servicio \_ SystemDriver de Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Método ChangeStartMode de la Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062757"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Método ChangeStartMode de la clase \_ SystemDriver de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de un [**servicio \_ SystemDriver de Win32.**](win32-systemdriver.md)

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartMode* \[ En\]
</dt> <dd>

Modo de inicio del Windows base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("Arranque")


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("Automático")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio de la demanda** ("Manual")


</dt> <dd>

Servicio que va a iniciar el administrador de control de servicios cuando un proceso llame al [**método StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("Deshabilitado")


</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se modificó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Servicios dependientes en ejecución** (3)
</dt> <dt>

**Control de servicio no válido** (4)
</dt> <dt>

**El servicio no puede aceptar el control** (5)
</dt> <dt>

**Servicio no activo** (6)
</dt> <dt>

**Tiempo de espera de solicitud de** servicio (7)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Servicio ya en ejecución** (10)
</dt> <dt>

**Base de datos de servicio bloqueada** (11)
</dt> <dt>

**Dependencia de servicio eliminada** (12)
</dt> <dt>

**Error de dependencia del** servicio (13)
</dt> <dt>

**Servicio deshabilitado** (14)
</dt> <dt>

**Error de inicio de sesión de** servicio (15)
</dt> <dt>

**Servicio marcado para eliminación** (16)
</dt> <dt>

**Service No Thread** (17)
</dt> <dt>

**Dependencia circular de estado** (18)
</dt> <dt>

**Nombre duplicado de estado** (19)
</dt> <dt>

**Nombre de estado no válido** (20)
</dt> <dt>

**Parámetro Status Invalid** (21)
</dt> <dt>

**Cuenta de servicio de estado no válida** (22)
</dt> <dt>

**El servicio de estado existe** (23)
</dt> <dt>

**Servicio ya en pausa** (24)
</dt> <dt>

**Otros** (25 4294967295)
</dt> </dl>

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

 

