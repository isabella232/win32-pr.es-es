---
description: GetOrdinal no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2:: GetOrdinal (método) (Msident. h)'
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
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985683"
---
# <a name="iuseridentity2getordinal-method"></a>IUserIdentity2:: GetOrdinal (método)

\[**GetOrdinal** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Obtiene el número ordinal de esta identidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwOrdinal* \[ enuncia\]
</dt> <dd>

Tipo: **DWORD \** _

Un puntero a un valor _ *DWORD** que recibe el número ordinal de esta identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El ordinal determina el orden de las identidades en la lista de identidades, pero puede que no se conserven en las distintas operaciones de las identidades. Para obtener un valor único para una identidad, llame a [**GetCookie**](iuseridentity-getcookie.md).

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetCookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




