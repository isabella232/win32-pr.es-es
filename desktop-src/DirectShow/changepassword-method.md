---
description: El método DVDAdm. ChangePassword guarda una nueva contraseña de aplicación en el registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494525"
---
# <a name="changepassword-method"></a>ChangePassword (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.ChangePassword` método guarda una nueva contraseña de aplicación en el registro.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de inicio de sesión del usuario actual como una cadena. El objeto MSDVDAdm omite este parámetro. Vea la sección Comentarios.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Venda*
</dt> <dd>

Especifica la contraseña anterior del usuario como una cadena.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Especifica la nueva contraseña del usuario como una cadena. No puede ser una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Actualmente, el parámetro *sUserName* se omite en este y todos los métodos relacionados. Esto significa que quien sabe que la contraseña puede establecer el nivel parental. Solo hay una contraseña y un nivel parental para la aplicación. No se admiten nombres de inicio de sesión de usuario individuales ni administración de varias contraseñas. Para aplicar los niveles de administración parental, los padres deben establecer la contraseña y, a continuación, establecer el nivel parental adecuado para los miembros jóvenes del grupo de familiares. Cuando los padres quieren ver un disco con contenido clasificado por adultos, pueden cambiar el nivel y, a continuación, cambiarlo de nuevo cuando hayan terminado de verlo. Siempre que los elementos secundarios no conozcan la contraseña, solo podrán ver el contenido en el nivel establecido o debajo de él.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



