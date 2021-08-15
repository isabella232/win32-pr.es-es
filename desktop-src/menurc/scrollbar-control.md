---
title: Control SCROLLBAR
description: Define un control de barra de desplazamiento.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menús de control SCROLLBAR y otros recursos
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733443"
---
# <a name="scrollbar-control"></a>Control SCROLLBAR

Define un control de barra de desplazamiento. El control es un rectángulo que contiene un cuadro de desplazamiento y tiene flechas de dirección en ambos extremos. El control de barra de desplazamiento envía un mensaje de notificación a su elemento primario cada vez que el usuario hace clic en el mouse en el control. El elemento primario es responsable de actualizar la posición del cuadro de desplazamiento. Los controles de barra de desplazamiento se pueden colocar en cualquier lugar de una ventana y usarse siempre que sea necesario para proporcionar una entrada de desplazamiento.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Cero o una combinación de los estilos siguientes: **WS \_ TABSTOP,** **WS \_ GROUP** y **WS \_ DISABLED.**

Además de estos estilos, el parámetro *style* puede contener una combinación (o ninguna) de los estilos de clase SCROLLBAR.

Si no especifica un estilo, el estilo predeterminado es **SBS \_ HORZ.**

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md). Tenga en cuenta que no se puede especificar texto para este control.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción SCROLLBAR:**

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Barras de desplazamiento](../controls/about-scroll-bars.md)
</dt> </dl>

 

 