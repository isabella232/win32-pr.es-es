---
description: Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: Método IIdentityChangeNotify::QuerySwitchIdentities (Msident.h)
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
ms.openlocfilehash: 38469490db92278c82e7935e1078181010757dd22be220203361d2d4c18ef380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593085"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>IIdentityChangeNotify::QuerySwitchIdentities (método)

\[**QuerySwitchIdentities está** disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la consulta switch. Si el modificador debe continuar, devuelva S \_ OK. De lo contrario, devuelva E PROCESS CANCELLED SWITCH para indicar que se debe anular el modificador de \_ \_ identidad del \_ usuario.

## <a name="remarks"></a>Comentarios

Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando un usuario solicita que se cambien las identidades. Puede detener el modificador de identidad pendiente devolviendo el valor E \_ PROCESS \_ CANCELLED \_ SWITCH.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




