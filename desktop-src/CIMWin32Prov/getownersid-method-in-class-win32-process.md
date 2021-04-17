---
description: GetOwnerSid&\# 8194; El método de clase WMI recupera el identificador de seguridad (SID) del propietario de este proceso.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Método GetOwnerSid de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659476"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Método GetOwnerSid de la \_ clase Process de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera el identificador de seguridad (SID) para el propietario de este proceso.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SID* \[ de enuncia\]
</dt> <dd>

Devuelve el descriptor de identificador de seguridad para este proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**No se encontró la ruta de acceso** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de código de PowerShell [Buscar el usuario que ha iniciado sesión en un sistema remoto/s versión 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) se consultan equipos remotos para ver quién ha iniciado sesión.

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

[**\_Proceso Win32**](win32-process.md)
</dt> </dl>

 

