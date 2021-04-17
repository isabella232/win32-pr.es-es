---
title: Control DEFPUSHBUTTON
description: Define un control de botón de complemento predeterminado.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menús de control de DEFPUSHBUTTON y otros recursos
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676333"
---
# <a name="defpushbutton-control"></a>Control DEFPUSHBUTTON

Define un control de botón de complemento predeterminado. El control es un pequeño rectángulo con un contorno en negrita que representa la respuesta predeterminada del usuario. El texto especificado se muestra dentro del botón. El control resalta el botón de la manera habitual cuando el usuario hace clic con el mouse en él y envía un mensaje a su ventana primaria.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Texto que se va a centrar en el área rectangular del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación de los siguientes estilos: **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** y **WS \_ deshabilitados**.

Si no especifica un estilo, el estilo predeterminado es `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de botón de opción predeterminado con la etiqueta cancelar:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Botones de reenvío](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**BOTONES**](pushbutton-control.md)
</dt> <dt>

[**ÍNDICES**](radiobutton-control.md)
</dt> </dl>

 

 




