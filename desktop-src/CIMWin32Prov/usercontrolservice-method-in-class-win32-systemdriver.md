---
description: Intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Método UserControlService de la Win32_SystemDriver clase
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
ms.openlocfilehash: e64d4493e43e23b6826c81ac61ae90d64a236d7ffcace32bb29f53b5c0c039fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105065"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Método UserControlService de la clase \_ SystemDriver de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario a un servicio administrado por un controlador del sistema.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ControlCode* \[ En\]
</dt> <dd>

Especifica valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se aceptó la solicitud **UserControlService,** 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

