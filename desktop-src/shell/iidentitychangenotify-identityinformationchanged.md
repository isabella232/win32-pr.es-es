---
description: IdentityInformationChanged no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: Método IIdentityChangeNotify::IdentityInformationChanged (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 58e146812bb36a9ff8e692aa424f328abc6eb62e47b98abb1deef2b4e919af40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821925"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>IIdentityChangeNotify::IdentityInformationChanged (método)

\[**IdentityInformationChanged** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Se llama cuando ha cambiado la información sobre una identidad de usuario o cuando se ha agregado o eliminado una identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwType* 
</dt> <dd>

Tipo: **DWORD**

Valor que especifica el tipo de información modificada o la operación realizada en una identidad. Puede ser una combinación de los valores siguientes.

<dt>



 (IIC) \_ IDENTIDAD \_ ACTUAL \_ CAMBIADA)


</dt> <dd>

Se ha modificado la identidad actual.

</dd> <dt>



 (IIC) \_ IDENTITY \_ CHANGED)


</dt> <dd>

Se ha modificado una identidad.

</dd> <dt>



 (IIC) \_ IDENTITY \_ DELETED)


</dt> <dd>

Se ha eliminado una identidad.

</dd> <dt>



 (IIC) \_ IDENTITY \_ ADDED)


</dt> <dd>

Se ha agregado una nueva identidad.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando se haya modificado la lista de identidades de usuario del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 




