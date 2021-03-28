---
description: 'IEnumUserIdentity:: Clone no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity:: Clone (método) (Msident. h)'
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
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997673"
---
# <a name="ienumuseridentityclone-method"></a>IEnumUserIdentity:: Clone (método)

\[**IEnumUserIdentity:: Clone** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Obtiene una copia de la enumeración actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppenum* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Dirección de un puntero que recibe una copia de esta enumeración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un recuento interno que especifica la interfaz que se va a recuperar. El valor de este recuento se aplicará a la interfaz recibida por *ppenum*. Para restablecer el recuento, llame a [**IEnumUserIdentity:: RESET**](ienumuseridentity-reset.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity:: RESET**](ienumuseridentity-reset.md)
</dt> </dl>

 

 




