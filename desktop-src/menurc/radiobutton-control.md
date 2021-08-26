---
title: Control RADIOBUTTON
description: Define un control de botón de radio.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menús de control RADIOBUTTON y otros recursos
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b01d6b2313ec4b881f182fd4a4ca34cf5bbf713dca9f329173d1817132606d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952255"
---
# <a name="radiobutton-control"></a>Control RADIOBUTTON

Define un control de botón de radio. El control es un círculo pequeño que muestra el texto especificado junto a él, normalmente a su derecha. El control resalta el círculo y envía un mensaje a su ventana primaria cuando el usuario selecciona el botón. El control quita el resaltado y envía un mensaje cuando el botón se selecciona a continuación.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el botón de radio, que puede ser una combinación de estilos de clase BUTTON y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ DISABLED** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción RADIOBUTTON:**

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botones de radio](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 