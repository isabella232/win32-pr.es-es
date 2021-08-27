---
description: GetIdentityFolder no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: Método IUserIdentity::GetIdentityFolder (Msident.h)
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
ms.openlocfilehash: 20357dde27214177a454eb585dcd51182228c247da5aeae5ef887089b73ed85d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720611"
---
# <a name="iuseridentitygetidentityfolder-method"></a>IUserIdentity::GetIdentityFolder (método)

\[**GetIdentityFolder** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

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

*dwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Obligatorio. Valor que especifica si la carpeta asociada a esta identidad es itinerancia. Debe ser uno de los siguientes valores:

<dt>



 (GIF) \_ CARPETA \_ MÓVIL)


</dt> <dd>

La carpeta es itinerancia.

</dd> <dt>



 (GIF) \_ CARPETA \_ QUE NO ES \_ ITINERANCIA)


</dt> <dd>

La carpeta es local.

</dd> </dl> </dd> <dt>

*pszPath* \[ En\]
</dt> <dd>

Tipo: **WCHAR \***

Puntero a una cadena de caracteres anchos que recibe la ruta de acceso de la carpeta.

</dd> <dt>

*ulBuffSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Valor que especifica el tamaño de *pszPath.*

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

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




