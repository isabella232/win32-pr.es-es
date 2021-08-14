---
description: GetCookie no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: Método IUserIdentity::GetCookie (Msident.h)
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
ms.openlocfilehash: e8b4abb13735b2ce370623ad8e5b79a8d9830b34a3d566fb57c0539d6f2c6095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220122"
---
# <a name="iuseridentitygetcookie-method"></a>IUserIdentity::GetCookie (método)

\[**GetCookie** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Obtiene la cookie utilizada para identificar de forma única esta identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*puidCookie* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Puntero a un valor **GUID que** recibe la cookie usada para identificar de forma única esta identidad de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**GetOrdinal**](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




