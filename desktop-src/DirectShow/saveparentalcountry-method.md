---
description: El método DVDAdm. SaveParentalCountry guarda el nuevo país o región parental de la aplicación en el registro.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Método SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690481"
---
# <a name="saveparentalcountry-method"></a>Método SaveParentalCountry

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.SaveParentalCountry` método guarda el nuevo país o región parental de la aplicación en el registro.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Especifica el país o la región parental como un entero.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de usuario como una cadena. (Actualmente omitido).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método permite a un usuario que conoce la contraseña actual guardar en el registro un nuevo valor de país o región parental. Al igual que con todos los métodos de **MSDVDAdm**, este método no afecta al nivel actual del reproductor; solo cambia la configuración del registro, de modo que la próxima vez que se cree el objeto MSWebDVD, se abrirá con el nuevo país o región. Para cambiar el país o la región parental en el reproductor, llame a [**SelectParentalCountry**](selectparentalcountry-method.md), que no cambia la configuración del registro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




