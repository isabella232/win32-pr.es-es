---
description: 'IUserIdentityManager:: Logon no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager:: Logon (método) (Msident. h)'
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
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153602"
---
# <a name="iuseridentitymanagerlogon-method"></a>IUserIdentityManager:: Logon (método)

\[**IUserIdentityManager:: Logon** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Muestra una interfaz de usuario para el usuario, lo que permite al usuario elegir una identidad de usuario. Si se realiza correctamente, la identidad del usuario se iniciará y se recuperará.

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

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Un valor **hWnd** que identifica una ventana que se enviará al primer plano después de que se descarte la interfaz de usuario de inicio de sesión.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales para definir cómo se comportará la interfaz de usuario. Establezca en UIL \_ Force \_ UI para forzar que se muestre la interfaz de usuario, incluso si ya se ha elegido una identidad.

</dd> <dt>

*ppIdentity* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Dirección del puntero que recibe la identidad del usuario elegida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la operación de inicio de sesión. Si se realiza correctamente, devuelve S \_ correcto. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ cancelado por el usuario \_**</dt> </dl>      | El usuario canceló la operación de inicio de sesión desde la interfaz de usuario.<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | No se pudo crear la identidad del usuario.<br/>                                          |
| <dl> <dt>**E \_ inesperado**</dt> </dl>           | Error inesperado en la operación.<br/>                                               |
| <dl> <dt>**E \_ identidades \_ deshabilitadas**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/>                                   |
| <dl> <dt>**\_identidades \_ deshabilitadas**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/>                                   |
| <dl> <dt>**E \_ identidad \_ cambiando**</dt> </dl>   | El sistema está cambiando actualmente las identidades y no puede completar la operación.<br/> |



 

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager:: Logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




