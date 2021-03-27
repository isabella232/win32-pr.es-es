---
description: IdentityInformationChanged no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify:: IdentityInformationChanged (método) (Msident. h)'
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
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909521"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>IIdentityChangeNotify:: IdentityInformationChanged (método)

\[**IdentityInformationChanged** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

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

Valor que especifica el tipo de información que se ha cambiado o la operación realizada en una identidad. Puede ser una combinación de los valores siguientes.

<dt>



 (IIC \_ \_identidad actual \_ modificada)


</dt> <dd>

La identidad actual se ha modificado.

</dd> <dt>



 (IIC \_ IDENTIDAD \_ cambiada)


</dt> <dd>

Se ha modificado una identidad.

</dd> <dt>



 (IIC \_ IDENTIDAD \_ eliminada)


</dt> <dd>

Se ha eliminado una identidad.

</dd> <dt>



 (IIC \_ IDENTIDAD \_ agregada)


</dt> <dd>

Se ha agregado una nueva identidad.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando se ha modificado la lista de identidades de usuario en el sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 




