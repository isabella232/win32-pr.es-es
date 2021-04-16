---
title: WMPEFFECTS
description: Se trata de efectos predefinidos con los siguientes valores predeterminados.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Windows Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718848"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Se trata de **efectos** predefinidos con los siguientes valores predeterminados.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Observaciones

Se creará un elemento **Effects** que recorrerá los valores preestablecidos de visualización cuando el usuario haga clic en el control. También se extienden las visualizaciones cuando se cambia el tamaño del reproductor.

El valor preestablecido de visualización inicial mostrado es el seleccionado en el menú **Ver** en **visualizaciones**. Al cambiar la selección en este menú, se cambia automáticamente el valor preestablecido que muestra este elemento cuando el reproductor está en modo de máscara. El menú **Ver** se muestra en el modo completo del reproductor o cuando el atributo **View. TitleBar** está establecido en true en una máscara.

Todas las propiedades de este elemento **Effects** se pueden invalidar si se especifican de forma explícita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> </dl>

 

 





