---
title: TEXT. fontSmoothing
description: El atributo fontSmoothing especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Media Player de Windows TEXT. fontSmoothing
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698704"
---
# <a name="textfontsmoothing"></a>TEXT. fontSmoothing

El atributo **fontSmoothing** especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                          |
|-------|--------------------------------------|
| true  | El suavizado de fuentes está habilitado.           |
| false | Predeterminada. El suavizado de fuentes está deshabilitado. |



 

## <a name="remarks"></a>Observaciones

El suavizado de fuentes utiliza la característica de suavizado de contorno del sistema operativo. Si el suavizado de fuentes está habilitado y el sistema operativo admite el suavizado de contorno, Windows Media Player intenta suavizar el texto. No todas las fuentes admiten el suavizado de contorno. Windows Media Player 10 usa el método de suavizado de contorno ClearType de Windows XP.

-   **ADVERTENCIA** de El suavizado de fuentes sobre un color transparente puede hacer que el color transparente se mezcle en los caracteres. No se recomienda usar **fontSmoothing** si el texto se va a mostrar sobre una transparencia.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





