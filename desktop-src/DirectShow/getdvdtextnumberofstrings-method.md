---
description: El método GetDVDTextNumberOfStrings recupera el número de cadenas de texto disponibles para el idioma especificado.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Método GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061138"
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

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objeto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



