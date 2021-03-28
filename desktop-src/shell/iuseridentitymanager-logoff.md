---
description: No se admite el cierre de sesión y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'IUserIdentityManager:: Logoff (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984155"
---
# <a name="iuseridentitymanagerlogoff-method"></a>IUserIdentityManager:: Logoff (método)

\[No se admite el **cierre de sesión** y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

En desuso. Cierre la sesión actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Un valor **hWnd** que identifica una ventana que se incluirá en primer plano cuando se complete el cierre de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager:: Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




