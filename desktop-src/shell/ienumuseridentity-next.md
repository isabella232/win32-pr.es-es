---
description: IEnumUserIdentity::Next no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: Método IEnumUserIdentity::Next (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009405"
---
# <a name="ienumuseridentitynext-method"></a>IEnumUserIdentity::Next (Método)

\[**IEnumUserIdentity::Next** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

En desuso. Recupera una matriz de interfaces de identidad de usuario de la enumeración .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Valor **ULONG** que representa el número de interfaces que se recuperarán.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Dirección de un puntero que recibe las interfaces.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Dirección de un puntero que recibe el número de interfaces recuperadas correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

[**IEnumUserIdentity mantiene**](ienumuseridentity.md) un recuento interno que especifica qué interfaz se va a recuperar. Varias llamadas a este método no restablecerán este recuento. Para restablecer el recuento, llame a [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md). Para incrementar el recuento sin recuperar interfaces, llame a [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).

El valor de *celt* no debe superar el valor devuelto por [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
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

[**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
