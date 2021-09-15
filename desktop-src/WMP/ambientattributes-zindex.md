---
title: AmbientAttributes.zIndex
description: El atributo zIndex especifica o recupera el orden en el que se representa el control.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes.zIndex Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270431"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes.zIndex

El **atributo zIndex** especifica o recupera el orden en el que se representa el control.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**long**) con un valor predeterminado de cero. El intervalo es el de un entero largo con signo.

## <a name="remarks"></a>Observaciones

El mapa de bits de fondo **de una vista** o **subvista** tiene un índice z fijo de cero. Si desea que un control esté detrás del fondo, **zIndex** debe establecerse en un número negativo.

El índice z de **view** o **SUBVIEW** es un índice absoluto, mientras que el índice z de un control es relativo al índice z de **view** o **SUBVIEW** que lo contiene.

Los elementos **BROWSER** y **PLAYLIST** no admiten el atributo **zIndex.** No funcionará con el elemento **VIDEO** si *VIDEO*. **windowless** se establece en false, ni con el **elemento EFFECTS** si **EFFECTS**. **windowed** se establece en true.

**Los elementos BUTTONELEMENT** usan **zIndex** de **su BUTTONGROUP.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





