---
description: El método GetTitleParentalLevels recupera los niveles de administración parentales para el título especificado.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Método GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422899"
---
# <a name="gettitleparentallevels-method"></a>Método GetTitleParentalLevels

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetTitleParentalLevels` método recupera los niveles de administración parentales para el título especificado.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero cuyos bits individuales indican qué niveles de administración parentales (PML) están establecidos en el título especificado.

## <a name="remarks"></a>Observaciones

Un título puede tener capítulos o incluso segmentos cortos que tengan un PML diferente del PML general para el título. Use este método para determinar todas las PMLs que se detectarán al reproducir un título especificado. El entero devuelto es un conjunto de marcadores de bits que se definen como se muestra en la tabla siguiente. Realice una operación and bit a bit en *iLevels* y cada valor posible. Si la operación devuelve **true**, significa que PML se encontrará en algún punto de este título.



| Value  | Descripción          |
|--------|----------------------|
| 0x100  | Nivel parental de DVD 1 |
| 0x200  | Nivel parental de DVD 2 |
| 0x400  | Nivel parental de DVD 3 |
| 0x800  | DVD de nivel superior 4 |
| 0x1000 | Nivel parental de DVD 5 |
| 0x2000 | Nivel parental de DVD 6 |
| 0x4000 | Nivel parental de DVD 7 |
| 0x8000 | Nivel parental de DVD 8 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



