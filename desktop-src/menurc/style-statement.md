---
title: STYLE (instrucción)
description: Define el estilo de ventana del cuadro de diálogo. El estilo de ventana especifica si el cuadro es una ventana emergente o secundaria.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menús de instrucciones de estilo y otros recursos
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420653"
---
# <a name="style-statement"></a>STYLE (instrucción)

Define el estilo de ventana del cuadro de diálogo. El estilo de ventana especifica si el cuadro es una ventana emergente o secundaria.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Nombre del estilo de la ventana. Este parámetro puede ser un valor entero o una combinación de valores de estilo de ventana (como **WS \_ Caption** y **WS \_ SYSMENU**) y valores de estilo de cuadro de diálogo (como el **\_ centro de DS**).

</dd> </dl>

Para obtener una lista de estilos de ventana, vea [estilos de ventana](/windows/desktop/winmsg/window-styles). Para obtener una lista de estilos de cuadro de diálogo, vea [estilos de plantilla de cuadro de diálogo](../dlgbox/about-dialog-boxes.md). Si utiliza los valores de estilo de ventana o de cuadro de diálogo, debe incluir Windows. h.

 

 