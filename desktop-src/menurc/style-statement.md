---
title: STYLE , instrucción
description: Define el estilo de ventana del cuadro de diálogo. El estilo de ventana especifica si el cuadro es un elemento emergente o una ventana secundaria.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menús de instrucción STYLE y otros recursos
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d74ced35b6b5a2f6c04004fbd2e161df7ba16ff5111577835b93363291c114
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886774"
---
# <a name="style-statement"></a>STYLE , instrucción

Define el estilo de ventana del cuadro de diálogo. El estilo de ventana especifica si el cuadro es un elemento emergente o una ventana secundaria.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Nombre del estilo de la ventana. Este parámetro puede ser un valor entero o una combinación de valores de estilo de ventana (como **WS \_ CAPTION** y **WS \_ SYSMENU)** y valores de estilo de cuadro de diálogo (como **DS \_ CENTER**).

</dd> </dl>

Para obtener una lista de estilos de ventana, vea [Estilos de ventana](/windows/desktop/winmsg/window-styles). Para obtener una lista de estilos de cuadro de diálogo, vea [Estilos de plantilla de cuadro de diálogo](../dlgbox/about-dialog-boxes.md). Si usa los valores de estilo de ventana o cuadro de diálogo, debe incluir Windows.h.

 

 