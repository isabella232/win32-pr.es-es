---
description: La eliminación&\# 8194; El método de clase WMI elimina un trabajo programado.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153567"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a>Método Delete de la \_ clase Win32 ScheduledJob

El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un trabajo programado.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completado correctamente.**
</dt> <dd>

0

Se aceptó la solicitud.

</dd> <dt>

**No admitido**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tenía el acceso necesario.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Proceso interactivo.

</dd> <dt>

**No se encuentra la ruta de acceso**
</dt> <dd>

9

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Servicio no iniciado**
</dt> <dd>

22

La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**Otros**
</dt> <dd>

23 4294967295

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

[**Win32 \_ ScheduledJob**](win32-scheduledjob.md)
</dt> </dl>

 

