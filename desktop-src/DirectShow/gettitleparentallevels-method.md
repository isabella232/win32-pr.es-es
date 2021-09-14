---
description: El método GetTitleParentalLevels recupera los niveles de administración parental del título especificado.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: GetTitleParentalLevels (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061099"
---
# <a name="gettitleparentallevels-method"></a>GetTitleParentalLevels (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetTitleParentalLevels` método recupera los niveles de administración parental para el título especificado.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero cuyos bits individuales indican qué niveles de administración parental (PML) se establecen en el título especificado.

## <a name="remarks"></a>Observaciones

Un título puede tener capítulos o incluso segmentos cortos que tienen una PML diferente de la PML general del título. Use este método para determinar todas las PML que se encontrarán al reproducir un título especificado. El entero devuelto es un conjunto de marcas de bits que se definen como se muestra en la tabla siguiente. Realice una operación AND bit a bit en *iLevels* y cada valor posible. Si la operación devuelve **true**, significa que la PML se encontrará en algún momento de este título.



| Value  | Descripción          |
|--------|----------------------|
| 0x100  | DVD Parental Level 1 |
| 0x200  | Dvd Parental Level 2 |
| 0x400  | DVD Parental Level 3 |
| 0x800  | DVD Parental Level 4 |
| 0x1000 | DVD Parental Level 5 |
| 0x2000 | DVD Parental Level 6 |
| 0x4000 | DVD Parental Level 7 |
| 0x8000 | DVD Parental Level 8 |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SeleccioneParentalLevel.**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SeleccioneParentalCountry.**](selectparentalcountry-method.md)
</dt> </dl>

 

 



