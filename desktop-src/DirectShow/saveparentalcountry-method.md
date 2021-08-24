---
description: El método DVDAdm.SaveParentalCountry guarda el nuevo país o región parental de la aplicación en el registro.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Método SaveParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5391982129c799e6a565da362837a557765cf46604653f4f702ed38dcb910e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651215"
---
# <a name="saveparentalcountry-method"></a>SaveParentalCountry (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método guarda el nuevo país o región parental de la `DVDAdm.SaveParentalCountry` aplicación en el registro.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Especifica el país o región parental como entero.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de usuario como una cadena. (Actualmente se omite).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método permite a un usuario que conoce la contraseña actual guardar una nueva configuración de país o región parental en el registro. Al igual que con todos los **métodos de MSDVDAdm**, este método no afecta al nivel actual del reproductor; solo cambia la configuración del Registro, de modo que la próxima vez que se cree el objeto MSWebDVD, se abrirá con el nuevo país o región. Para cambiar el país o región parental del reproductor, llame a [**SelectParentalCountry**](selectparentalcountry-method.md), que no cambia la configuración del Registro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




