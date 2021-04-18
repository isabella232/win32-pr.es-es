---
title: AmbientAttributes. zIndex
description: El atributo zIndex especifica o recupera el orden en el que se representa el control.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Media Player de Windows AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700091"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes. zIndex

El atributo **ZIndex** especifica o recupera el orden en el que se representa el control.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (**Long**) con un valor predeterminado de cero. El intervalo es el de un entero largo con signo.

## <a name="remarks"></a>Observaciones

El mapa de bits de fondo de una **vista** o una **subvista** tiene un índice z fijo de cero. Si desea que un control esté detrás del fondo, el valor de **ZIndex** debe establecerse en un número negativo.

El índice z de una **vista** o una **subvista** es un índice absoluto, mientras que el índice z de un control es relativo al índice z de la **vista** o la **subvista** que lo contiene.

El atributo **ZIndex** no es compatible con los elementos de la **lista de reproducción** y el **Explorador** . No funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene **efectos**. **windowed** está establecido en true.

Los elementos **BUTTONELEMENT** usan el **ZIndex** de sus **BUTTONGROUP**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





