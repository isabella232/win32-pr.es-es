---
description: El método DVDAdm.ChangePassword guarda una nueva contraseña de aplicación en el Registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999335"
---
# <a name="changepassword-method"></a>ChangePassword (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.ChangePassword` método guarda una nueva contraseña de aplicación en el Registro.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de inicio de sesión del usuario actual como string. El objeto MSDVDAdm omite este parámetro. Vea la sección Comentarios.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Vendido*
</dt> <dd>

Especifica la contraseña antigua del usuario como una cadena.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Especifica la nueva contraseña del usuario como una cadena. No puede ser una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Actualmente, el *parámetro sUserName* se omite en este y en todos los métodos relacionados. Esto significa que quien conoce la contraseña puede establecer el nivel parental. Solo hay una contraseña y un nivel parental para la aplicación. No se admiten nombres de inicio de sesión de usuario individuales ni administración de varias contraseñas. Para aplicar los niveles de administración parental, los padres deben establecer la contraseña y, a continuación, establecer el nivel parental adecuado para los miembros más pequeños del grupo de familiares. Cuando los padres desean ver un disco con contenido clasificado para adultos, pueden cambiar el nivel y, a continuación, cambiarlo de nuevo cuando terminen de verlo. Siempre que los secundarios no conozcan la contraseña, solo pueden ver contenido en el nivel establecido para ellos o por debajo de él.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



