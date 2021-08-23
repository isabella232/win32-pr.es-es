---
description: Solicita que el servicio del controlador del sistema actualice su estado al administrador de servicios.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Método InterrogateService de la Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0327dc7dcb357217ff18df85b22c7cc7bff8972f42ebeb53a89f552c98205d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760335"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a>Método InterrogateService de la clase \_ SystemDriver de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio del controlador del sistema actualice su estado al administrador de servicios.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se aceptó la solicitud **InterrogateService,** 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**BaseService de Win32 \_**](win32-baseservice.md)
</dt> </dl>

 

