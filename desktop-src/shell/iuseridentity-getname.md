---
description: IUserIdentity::GetName no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: Método IUserIdentity::GetName (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 035f7c61290fb60e70821f0a43676c41dca0fc92cebc8ecfb963bb757ab47a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661195"
---
# <a name="iuseridentitygetname-method"></a>IUserIdentity::GetName (método)

\[**IUserIdentity::GetName** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Obtiene el nombre asociado a esta identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszName* \[ En\]
</dt> <dd>

Tipo: **WCHAR \***

Puntero a una cadena de caracteres anchos que recibe el nombre de esta identidad de usuario.

</dd> <dt>

*ulBuffSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Valor que especifica el tamaño de *pszName.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**SetName**](iuseridentity2-setname.md)
</dt> </dl>

 

 




