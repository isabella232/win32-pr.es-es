---
description: 'Método Delete de la Win32_SystemDriver : el&\# 8194; El método de clase WMI elimina un servicio existente.'
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Método Delete de la Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061536"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a>Método Delete de la clase \_ SystemDriver de Win32

El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se eliminó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

 

