---
description: GetCookie no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'IUserIdentity:: GetCookie (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984618"
---
# <a name="iuseridentitygetcookie-method"></a>IUserIdentity:: GetCookie (método)

\[**GetCookie** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Obtiene la cookie usada para identificar de forma única esta identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*puidCookie* \[ enuncia\]
</dt> <dd>

Tipo: **GUID \** _

Un puntero a un valor _ *GUID** que recibe la cookie usada para identificar de forma única esta identidad de usuario.

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

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**GetOrdinal**](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




