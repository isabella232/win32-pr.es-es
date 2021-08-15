---
description: GetOrdinal no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: Método IUserIdentity2::GetOrdinal (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d5453a083a1db23e042d24c3da4cd2948ff70f813fcc9026a00324eade467918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968974"
---
# <a name="iuseridentity2getordinal-method"></a>IUserIdentity2::GetOrdinal (método)

\[**GetOrdinal no** se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Obtiene el número ordinal de esta identidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwOrdinal* \[ out\]
</dt> <dd>

Tipo: **DWORD \***

Puntero a un **valor DWORD** que recibe el número ordinal de esta identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El ordinal determina el orden de las identidades en la lista de identidades, pero puede que no se conserve a lo largo de las operaciones en las identidades. Para obtener un valor único para una identidad, llame a [**GetCookie**](iuseridentity-getcookie.md).

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

[**GetCookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




