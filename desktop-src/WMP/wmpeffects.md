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
ms.openlocfilehash: e84f33833e9d69c39cb50ff81bd6c97ff8f79d1e2f881f82d6e4d293e78d87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761275"
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

## <a name="remarks"></a>Comentarios

Esto creará un elemento **EFFECTS** que pasará por los valores preestablecidos de visualización cuando el usuario haga clic en el control. También ajustará las visualizaciones cuando se cambie el tamaño del reproductor.

El valor preestablecido de visualización inicial que se muestra es el seleccionado en el **menú Ver** en **Visualizaciones.** Al cambiar la selección de este menú, se cambiará automáticamente el valor preestablecido que muestra este elemento cuando el reproductor está en modo de máscara. El **menú** Ver se muestra en el modo completo del reproductor o cuando el atributo **VIEW.titleBar** se establece en true en una máscara.

Todas las propiedades de **este elemento EFFECTS** se pueden invalidar especificándolos explícitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO EFFECTS**](effects-element.md)
</dt> </dl>

 

 





