---
description: IUserIdentityManager::Logon no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: Método IUserIdentityManager::Logon (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e5be9402dbbbf7c46528ceeab944317fa35857f9521db41b621ab246c8da86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821135"
---
# <a name="iuseridentitymanagerlogon-method"></a>IUserIdentityManager::Logon (método)

\[**IUserIdentityManager::Logon** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Muestra una interfaz de usuario al usuario, lo que permite al usuario elegir una identidad de usuario. Si se realiza correctamente, la identidad del usuario se inicia sesión y se recupera.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Valor **HWND que** identifica una ventana que se pondrá en primer plano después de descartar la interfaz de usuario de inicio de sesión.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales para definir cómo se comportará la interfaz de usuario. Establezca en UIL FORCE UI para forzar la presentación de la interfaz de usuario, incluso si ya se \_ ha elegido una \_ identidad.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Dirección del puntero que recibe la identidad de usuario elegida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la operación de inicio de sesión. Si se realiza correctamente, devuelve S \_ OK. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ USER \_ CANCELLED**</dt> </dl>      | El usuario canceló la operación de inicio de sesión de la interfaz de usuario.<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | No se pudo crear la identidad del usuario.<br/>                                          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Error inesperado en la operación.<br/>                                               |
| <dl> <dt>**IDENTIDADES \_ E \_ DESHABILITADAS**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/>                                   |
| <dl> <dt>**IDENTIDADES DE S \_ \_ DESHABILITADAS**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/>                                   |
| <dl> <dt>**CAMBIO \_ DE IDENTIDAD \_ E**</dt> </dl>   | El sistema está cambiando actualmente las identidades y no puede completar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




