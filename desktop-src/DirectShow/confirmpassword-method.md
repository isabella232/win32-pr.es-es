---
description: El método DVDAdm.ConfirmPassword comprueba si la contraseña especificada coincide con la contraseña guardada anteriormente.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Método ConfirmPassword (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161588"
---
# <a name="confirmpassword-method"></a>ConfirmPassword (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.ConfirmPassword` método comprueba si la contraseña especificada coincide con la contraseña guardada anteriormente.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre del usuario como string.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la nueva contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve true si la contraseña especificada coincide con la contraseña existente; de lo contrario, false.

## <a name="remarks"></a>Observaciones

Actualmente, el *parámetro sUserName* se omite en este y en todos los métodos relacionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




