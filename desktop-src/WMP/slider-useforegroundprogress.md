---
title: SLIDEr. useForegroundProgress
description: El atributo useForegroundProgress especifica o recupera un valor que indica si se utilizará la barra de progreso en primer plano.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- CONTROL SLIDEr. useForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660289"
---
# <a name="slideruseforegroundprogress"></a>SLIDEr. useForegroundProgress

El atributo **useForegroundProgress** especifica o recupera un valor que indica si se utilizará la barra de progreso en primer plano.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                              |
|-------|------------------------------------------|
| true  | Usar el progreso en primer plano.                 |
| false | Predeterminada. No usar el progreso en primer plano. |



 

## <a name="remarks"></a>Observaciones

Este atributo permite el uso del atributo **foregroundProgress** , que se usa principalmente para realizar el seguimiento del progreso de la descarga de un archivo multimedia mientras se realiza un seguimiento simultáneo de la posición de reproducción actual del archivo mediante el atributo **Value** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**Control deslizante. valor**](slider-value.md)
</dt> </dl>

 

 





