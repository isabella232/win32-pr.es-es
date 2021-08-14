---
description: IUserIdentity2::SetName no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: Método IUserIdentity2::SetName (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 32c375f37fbc0bc6352a79c9eb37be56578b236f6131c4ead1ea721cc53ce5e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220077"
---
# <a name="iuseridentity2setname-method"></a>IUserIdentity2::SetName (método)

\[**IUserIdentity2::SetName** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

Establece el nombre para mostrar de la identidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszName* \[ En\]
</dt> <dd>

Tipo: **WCHAR \***

Cadena de caracteres anchos que contiene el nuevo nombre de la identidad.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetName**](iuseridentity-getname.md)
</dt> </dl>

 

 




