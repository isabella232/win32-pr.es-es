---
description: No se admite el cierre de sesión y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: Método IUserIdentityManager::Logoff (Msident.h)
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
ms.openlocfilehash: 6011bf839e2f91b3eb835cfe295e0c1845a6c6697a262c0f9bf7525d6c157565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884065"
---
# <a name="iuseridentitymanagerlogoff-method"></a>IUserIdentityManager::Logoff (método)

\[**No se** admite el cierre de sesión y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

En desuso. Cierre la sesión de la identidad actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Valor **HWND** que identifica una ventana que se pondrá en primer plano cuando se complete el cierre de sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




