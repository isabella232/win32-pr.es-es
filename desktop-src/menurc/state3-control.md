---
title: Control STATE3
description: Define un control de casilla de tres Estados. El control es idéntico al de una casilla, con la excepción de que tiene tres Estados activado, desactivado y deshabilitado (atenuado).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menús de control de STATE3 y otros recursos
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783665"
---
# <a name="state3-control"></a>Control STATE3

Define un control de casilla de tres Estados. El control es idéntico a una [**casilla**](checkbox-control.md), excepto en que tiene tres Estados: checked, unchecked y Disabled (atenuado).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Texto que se va a mostrar a la derecha del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación del estilo de clase de botón **BS \_ 3STATE** y los estilos de **WS \_ TABSTOP** y de **\_ Grupo WS** .

Si no especifica un estilo, el estilo predeterminado es `BS_3STATE | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Autocheckbox**](autocheckbox-control.md)
</dt> <dt>

[Casillas](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**CASILLA**](checkbox-control.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> </dl>

 

 




