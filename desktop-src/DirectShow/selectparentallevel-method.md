---
description: El método SelectParentalLevel establece el nivel parental especificado para su posterior reproducción.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Método SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537107"
---
# <a name="selectparentallevel-method"></a>Método SelectParentalLevel

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectParentalLevel` método establece el nivel parental especificado para su posterior reproducción.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica el nivel de administración parental como un entero. Para habilitar la administración parental, el parámetro *iLevel* debe oscilar entre 1 y 8. Para deshabilitar la administración parental, establezca *iLevel* en-1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el usuario actual como una cadena. (Actualmente omitido).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña almacenada actualmente en el registro como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece el nivel de acceso en el objeto MSWebDVD, que determina el contenido que el usuario puede reproducir. Los niveles superiores pueden reproducir contenido de nivel inferior, pero los niveles inferiores no pueden reproducir contenido de nivel superior. El significado exacto de los ocho niveles de administración parental varía en función del país o la región. En el Estados Unidos y Canadá, los niveles se asignan a las categorías de clasificación de la Asociación de imágenes de movimiento (MPAA). La administración parental en el navegador de DVD está deshabilitada de forma predeterminada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



