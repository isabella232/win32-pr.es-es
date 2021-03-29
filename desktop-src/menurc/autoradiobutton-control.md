---
title: Control autoradiobutton
description: Define un control de botón de radio automático. Este control realiza automáticamente la exclusión mutua con los demás controles autoradiobutton del mismo grupo. Cuando se elige el botón, se notifica a la aplicación con el BN en el que se \_ hace clic.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menús de control autoradiobutton y otros recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783887"
---
# <a name="autoradiobutton-control"></a>Control autoradiobutton

Define un control de botón de radio automático. Este control realiza automáticamente la exclusión mutua con los demás controles **AUTOradiobutton** del mismo grupo. Cuando se elige el botón, se notifica a la aplicación con el BN en el que se **\_ hace clic**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Texto que aparecerá junto al botón de radio.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos para el botón de radio automático, que puede ser una combinación de estilos de clase de botón y los estilos siguientes: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Botones de radio](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**ÍNDICES**](radiobutton-control.md)
</dt> </dl>

 

 




