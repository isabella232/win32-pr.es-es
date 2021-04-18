---
title: VER. titleBar
description: El atributo titleBar recupera un valor que indica si se muestra la barra de título de la ventana.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- Ver ventanas de Media Player. titleBar
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718733"
---
# <a name="viewtitlebar"></a>VER. titleBar

El atributo **TitleBar** recupera un valor que indica si se muestra la barra de título de la ventana.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de solo lectura.



| Value | Descripción                             |
|-------|-----------------------------------------|
| true  | Predeterminada. Se muestra la barra de título de la ventana. |
| false | No se muestra la barra de título de la ventana.      |



 

## <a name="remarks"></a>Observaciones

Si se muestra la barra de título, se mostrarán los botones cuadro de control, minimizar y cerrar. El título de la ventana será el título del elemento de **vista** .

Si **TitleBar** está establecido en true y el usuario intenta cambiar el valor de **video. zoom**, el cambio no tendrá lugar a menos que la máscara supervise el **zoom** y tome las medidas adecuadas para cambiar el tamaño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> <dt>

[**VER. título**](view-title.md)
</dt> <dt>

[**VÍDEO. zoom**](video-zoom.md)
</dt> </dl>

 

 





