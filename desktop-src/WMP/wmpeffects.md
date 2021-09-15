---
title: WMPEFFECTS
description: Se trata de un effects predefinido con los siguientes valores predeterminados.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579381"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Se trata de un **effects** predefinido con los siguientes valores predeterminados.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Observaciones

Esto creará un elemento **EFFECTS** que pasará por los valores preestablecidos de visualización cuando el usuario haga clic en el control. También ajustará las visualizaciones cuando se cambie el tamaño del reproductor.

El valor preestablecido de visualización inicial que se muestra es el seleccionado en el **menú Ver** en **Visualizaciones.** Al cambiar la selección en este menú, se cambiará automáticamente el valor preestablecido que muestra este elemento cuando el reproductor está en modo de máscara. El **menú** Ver se muestra en el modo completo del reproductor o cuando el atributo **VIEW.titleBar** se establece en true en una máscara.

Todas las propiedades de **este elemento EFFECTS** se pueden invalidar si se especifican explícitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTS, elemento**](effects-element.md)
</dt> </dl>

 

 





