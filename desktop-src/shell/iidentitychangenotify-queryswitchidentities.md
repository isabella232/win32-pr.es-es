---
description: Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify:: QuerySwitchIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909518"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>IIdentityChangeNotify:: QuerySwitchIdentities (método)

\[**QuerySwitchIdentities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la consulta switch. Si el conmutador debe continuar, vuelva a ser \_ correcto. De lo contrario, devuelva \_ \_ el modificador de proceso cancelado \_ para indicar que se debe anular el cambio de identidad del usuario.

## <a name="remarks"></a>Observaciones

Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando un usuario solicita que se cambien las identidades. Puede detener el cambio de identidad pendiente devolviendo el valor E \_ proceso \_ cancelado \_ .

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




