---
description: Intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000763"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Método UserControlService de la \_ clase SystemDriver de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.

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

Especifica los valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se aceptó la solicitud **UserControlService** , 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

 

