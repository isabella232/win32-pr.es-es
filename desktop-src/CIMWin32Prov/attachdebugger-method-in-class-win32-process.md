---
description: Inicia el depurador actualmente registrado para este proceso.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Método AttachDebugger de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907050"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Método AttachDebugger de la \_ clase Process de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** inicia el depurador actualmente registrado para este proceso.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completado correctamente.**
</dt> <dd>

0

Finalización correcta.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tiene acceso a la información solicitada.

</dd> <dt>

**Privilegio insuficiente**
</dt> <dd>

3

El usuario no tiene privilegios suficientes.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Error desconocido.

</dd> <dt>

**No se encuentra la ruta de acceso**
</dt> <dd>

9

La ruta especificada no existe.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

El parámetro especificado no es válido.

</dd> <dt>

**Otros**
</dt> <dd>

22 4294967295

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

[**\_Proceso Win32**](win32-process.md)
</dt> </dl>

 

