---
description: ChangePassword no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2:: ChangePassword (método) (Msident. h)'
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
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984606"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2:: ChangePassword (método)

\[**ChangePassword** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

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

*szOldPass* \[ de\]
</dt> <dd>

Tipo: **WCHAR \** _

Cadena de caracteres anchos que contiene la contraseña asociada actualmente a la identidad.

</dd> <dt>

_szNewPass * \[ en\]
</dt> <dd>

Tipo: **WCHAR \** _

Cadena de caracteres anchos que contiene la nueva contraseña que se va a asociar a la identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El valor de *szOldPass* debe coincidir con la contraseña actual de la identidad de *szNewPass* que se va a aplicar. Un valor incorrecto de *szOldPass* producirá un error en un valor devuelto de E \_ .

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



 

 




