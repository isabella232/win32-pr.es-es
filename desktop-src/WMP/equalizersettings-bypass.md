---
title: EQUALIZERSETTINGS.bypass
description: El atributo bypass especifica o recupera un valor que indica si el filtro de igualador se omite en el gráfico de filtros.
ms.assetid: b189a6f1-e0d0-4cfa-9a99-73d3ccd705e0
keywords:
- EQUALIZERSETTINGS.bypass Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.bypass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b78fe6f4ce7608ff02ecb5b125b00171610ec112
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241028"
---
# <a name="equalizersettingsbypass"></a>EQUALIZERSETTINGS.bypass

El **atributo bypass** especifica o recupera un valor que indica si el filtro de equalizer se omite en el gráfico de filtros.

``` syntax
        elementID.bypass
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                |
|-------|--------------------------------------------|
| true  | Predeterminada. Se omite el filtro del igualador. |
| false | Se usa el filtro de igualador.              |



 

## <a name="remarks"></a>Observaciones

Si no se especifica este atributo, se conservará el valor anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> </dl>

 

 





