---
description: GetOwnerSid&\# 8194; El método de clase WMI recupera el identificador de seguridad (SID) del propietario de este proceso.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Método GetOwnerSid de la Win32_Process clase
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
ms.openlocfilehash: 2884c0f1cd3cc6e32a2db1ab14824ba3112624002cb10f4d76782d622e069000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918385"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Método GetOwnerSid de la clase Process de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera el identificador de seguridad (SID) del propietario de este proceso.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Sid* \[ out\]
</dt> <dd>

Devuelve el descriptor de identificador de seguridad para este proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otros** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de código Buscar los usuarios que han iniciado sesión en un sistema remoto o versión [2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) de PowerShell se consultan las máquinas remotas para ver quién ha iniciado sesión.

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

[**Proceso \_ win32**](win32-process.md)
</dt> </dl>

 

