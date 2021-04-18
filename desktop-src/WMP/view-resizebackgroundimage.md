---
title: VER. resizeBackgroundImage
description: El atributo resizeBackgroundImage especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- VIEW. resizeBackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718608"
---
# <a name="viewresizebackgroundimage"></a>VER. resizeBackgroundImage

El atributo **resizeBackgroundImage** especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Valores | Descripción                                      |
|--------|--------------------------------------------------|
| true   | Se puede cambiar el tamaño de la imagen de fondo.             |
| false  | Predeterminada. No se puede cambiar el tamaño de la imagen de fondo. |



 

## <a name="remarks"></a>Observaciones

Si establece este atributo en true, la imagen de fondo cambiará de tamaño para ajustarse a los valores actuales de los atributos de **ancho** y **alto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> <dt>

[**VIEW. backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





