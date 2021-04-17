---
description: El método DVDAdm. ConfirmPassword comprueba si la contraseña especificada coincide con la contraseña guardada previamente.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Método ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670985"
---
# <a name="confirmpassword-method"></a>Método ConfirmPassword

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.ConfirmPassword` método comprueba si la contraseña especificada coincide con la contraseña guardada previamente.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre del usuario como una cadena.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la nueva contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve true si la contraseña especificada coincide con la contraseña existente; de lo contrario, devuelve false.

## <a name="remarks"></a>Observaciones

Actualmente, el parámetro *sUserName* se omite en este y todos los métodos relacionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




