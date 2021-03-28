---
description: 'IUserIdentityManager:: ManageIdentities no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager:: ManageIdentities (método) (Msident. h)'
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
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360086"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>IUserIdentityManager:: ManageIdentities (método)

\[**IUserIdentityManager:: ManageIdentities** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Muestra una interfaz de usuario para el usuario, lo que permite al usuario administrar las identidades de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Un valor **hWnd** que identifica una ventana que se va a devolver al primer plano después de que se descarte la interfaz de usuario.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Marcas opcionales para definir cómo se comportará la interfaz de usuario. Establezca en UIMI \_ crear \_ nueva \_ identidad para solicitar al usuario que cree una nueva identidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la operación de administración. Si se realiza correctamente, devuelve S \_ correcto. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E \_ identidades \_ deshabilitadas**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/> |
| <dl> <dt>**E \_ cancelado por el usuario \_**</dt> </dl>      | El usuario canceló el cuadro de diálogo.<br/>                  |



 

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

[**IUserIdentityManager:: Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager:: Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




