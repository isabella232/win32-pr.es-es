---
title: Control AUTORADIOBUTTON
description: Define un control de botón de radio automático. Este control realiza automáticamente la exclusión mutua con los demás controles AUTORADIOBUTTON del mismo grupo. Cuando se elige el botón, se notifica a la aplicación con BN \_ CLICKED.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menús de control AUTORADIOBUTTON y otros recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468561"
---
# <a name="autoradiobutton-control"></a>Control AUTORADIOBUTTON

Define un control de botón de radio automático. Este control realiza automáticamente la exclusión mutua con los demás **controles AUTORADIOBUTTON** del mismo grupo. Cuando se elige el botón, se notifica a la aplicación con **BN \_ CLICKED**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que aparecerá junto al botón de radio.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el botón de radio automático, que puede ser una combinación de estilos de clase BUTTON y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ DISABLED** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Botones de radio](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




