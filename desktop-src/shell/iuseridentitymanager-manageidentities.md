---
description: IUserIdentityManager::ManageIdentities no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: Método IUserIdentityManager::ManageIdentities (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a816ee16e128b992b18be274d814fe3369e1a59c0204201a9c6bd4a6cbc23857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859243"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>IUserIdentityManager::ManageIdentities (método)

\[**IUserIdentityManager::ManageIdentities** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

Muestra una interfaz de usuario al usuario, lo que permite al usuario administrar las identidades de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Valor **HWND** que identifica una ventana que se pondrá en primer plano después de descartar la interfaz de usuario.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales para definir cómo se comportará la interfaz de usuario. Establezca en UIMI \_ CREATE NEW IDENTITY para solicitar al usuario que cree una nueva \_ \_ identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la operación de administración. Si se realiza correctamente, devuelve S \_ OK. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**IDENTIDADES \_ E \_ DESHABILITADAS**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/> |
| <dl> <dt>**E \_ USER \_ CANCELLED**</dt> </dl>      | El usuario canceló el cuadro de diálogo.<br/>                  |



 

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




