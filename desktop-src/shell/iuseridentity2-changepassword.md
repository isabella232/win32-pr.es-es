---
description: ChangePassword no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: Método IUserIdentity2::ChangePassword (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092702"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2::ChangePassword (método)

\[**ChangePassword** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

Establece una nueva contraseña para la identidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szOldPass* \[ En\]
</dt> <dd>

Tipo: **WCHAR \***

Cadena de caracteres anchos que contiene la contraseña asociada actualmente a la identidad.

</dd> <dt>

*szNewPass* \[ En\]
</dt> <dd>

Tipo: **WCHAR \***

Cadena de caracteres anchos que contiene la nueva contraseña que se va a asociar a la identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El valor de *szOldPass* debe coincidir con la contraseña actual de la identidad para *que se aplique szNewPass.* Un valor incorrecto de *szOldPass* dará como resultado un valor devuelto de E \_ FAIL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




