---
description: GetIdentityFolder no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'IUserIdentity:: GetIdentityFolder (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984611"
---
# <a name="iuseridentitygetidentityfolder-method"></a>IUserIdentity:: GetIdentityFolder (método)

\[**GetIdentityFolder** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Obtiene la carpeta de archivos asociada a esta identidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Obligatorio. Valor que especifica si la carpeta asociada a esta identidad es roaming. Debe ser uno de los valores siguientes.

<dt>



 (GIF \_ ) carpeta móvil \_ )


</dt> <dd>

La carpeta está en itinerancia.

</dd> <dt>



 (GIF \_ ) \_carpeta no móvil \_ )


</dt> <dd>

La carpeta es local.

</dd> </dl> </dd> <dt>

*pszPath* \[ de\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntero a una cadena de caracteres anchos que recibe la ruta de acceso de la carpeta.

</dd> <dt>

_ulBuffSize * \[ en\]
</dt> <dd>

Tipo: **ULong**

Valor que especifica el tamaño de *pszPath*.

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

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




