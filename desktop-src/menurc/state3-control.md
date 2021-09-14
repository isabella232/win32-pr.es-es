---
title: Control STATE3
description: Define un control de casilla de tres estados. El control es idéntico a un CHECKBOX, salvo que tiene tres estados activados, desactivados y deshabilitados (atenuados).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menús de control STATE3 y otros recursos
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268471"
---
# <a name="state3-control"></a>Control STATE3

Define un control de casilla de tres estados. El control es idéntico a [**un checkbox**](checkbox-control.md), salvo que tiene tres estados: activado, desactivado y deshabilitado (atenuado).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que se va a mostrar a la derecha del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación del estilo de clase de botón **BS \_ 3STATE** y los estilos **\_ TABSTOP** y **WS \_ GROUP de WS.**

Si no especifica un estilo, el estilo predeterminado es `BS_3STATE | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Casillas](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**CASILLA**](checkbox-control.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> </dl>

 

 




