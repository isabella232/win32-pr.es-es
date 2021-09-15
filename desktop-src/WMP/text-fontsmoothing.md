---
title: TEXT.fontSmoothing
description: El atributo fontSmoothing especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- TEXT.fontSmoothing Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360170"
---
# <a name="textfontsmoothing"></a>TEXT.fontSmoothing

El **atributo fontSmoothing** especifica o recupera un valor que indica si está habilitado el suavizado de fuentes.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                          |
|-------|--------------------------------------|
| true  | El suavizado de fuentes está habilitado.           |
| false | Predeterminada. El suavizado de fuentes está deshabilitado. |



 

## <a name="remarks"></a>Observaciones

El suavizado de fuentes usa la característica de suavizado de alias del sistema operativo. Si el suavizado de fuentes está habilitado y el sistema operativo admite suavizado de alias, Reproductor de Windows Media intenta suavizar el texto. No todas las fuentes admiten suavizado de alias. Reproductor de Windows Media 10 usa el método Windows suavizado de alias XP ClearType.

-   **Advertencia** El suavizado de fuentes sobre un color transparente puede hacer que el color transparente se combine con los caracteres. No se recomienda usar **fontSmoothing si** el texto se mostrará sobre una transparencia.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





