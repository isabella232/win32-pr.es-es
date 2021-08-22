---
title: VIEW.titleBar
description: El atributo titleBar recupera un valor que indica si se muestra la barra de título de la ventana.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW.titleBar Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb05550c22c342d14690f24f42c62a3af328eae65201b8138e82a7a33bf99fb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054073"
---
# <a name="viewtitlebar"></a>VIEW.titleBar

El **atributo titleBar** recupera un valor que indica si se muestra la barra de título de la ventana.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de **solo lectura.**



| Valor | Descripción                             |
|-------|-----------------------------------------|
| true  | Predeterminada. Se muestra la barra de título de la ventana. |
| false | No se muestra la barra de título de la ventana.      |



 

## <a name="remarks"></a>Comentarios

Si se muestra la barra de título, se mostrarán los botones cuadro de control, minimizar y cerrar. El título de la ventana será el título del **elemento VIEW.**

Si **titleBar** se establece en true y el usuario intenta cambiar el valor de **Video.zoom**, el cambio no tendrá lugar a menos que la máscara monitore el **zoom** y tome las medidas adecuadas para cambiar el tamaño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> <dt>

[**VIEW.title**](view-title.md)
</dt> <dt>

[**VIDEO.zoom**](video-zoom.md)
</dt> </dl>

 

 





