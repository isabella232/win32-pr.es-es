---
description: Se llama cuando se cambian las identidades de usuario.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: Método IIdentityChangeNotify::SwitchIdentities (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4b03963f656f84197e6008b5fae33f6ca9f5963ce71959c16cf69ffd68d63d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049763"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a>IIdentityChangeNotify::SwitchIdentities (método)

\[**SwitchIdentities está** disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Se llama cuando se cambian las identidades de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando un usuario haya cambiado correctamente las identidades. Para proporcionar un comportamiento personalizado antes de que se produzca un cambio de identidad de usuario, implemente el método [**IIdentityChangeNotify::QuerySwitchIdentities.**](iidentitychangenotify-queryswitchidentities.md)

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




