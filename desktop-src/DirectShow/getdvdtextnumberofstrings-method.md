---
description: El método GetDVDTextNumberOfStrings recupera el número de cadenas de texto disponibles para el idioma especificado.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Método GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be6818d447ad244ec59be029f21119ef89024477edc7811de94372c3825fa25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537055"
---
# <a name="getdvdtextnumberofstrings-method"></a>Método GetDVDTextNumberOfStrings

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetDVDTextNumberOfStrings` método recupera el número de cadenas de texto disponibles para el idioma especificado.

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Especifica el idioma como entero. El valor debe oscilar entre cero y uno menos que el valor devuelto por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que especifica cuántas cadenas contiene el disco en el idioma especificado.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



