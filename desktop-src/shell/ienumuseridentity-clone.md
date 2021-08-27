---
description: IEnumUserIdentity::Clone no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: Método IEnumUserIdentity::Clone (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3e6b0903029fa44e26651ad1df99ceb0c6bd83253bcd1d139bb6513d65e3ca3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009415"
---
# <a name="ienumuseridentityclone-method"></a>IEnumUserIdentity::Clone (Método)

\[**IEnumUserIdentity::Clone** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

Obtiene una copia de la enumeración actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mio* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Dirección de un puntero que recibe una copia de esta enumeración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

[**IEnumUserIdentity mantiene**](ienumuseridentity.md) un recuento interno que especifica qué interfaz está al lado de la recuperación. El valor de este recuento se aplicará a la interfaz recibida por *la enumeración*. Para restablecer el recuento, llame a [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> </dl>

 

 




