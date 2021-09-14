---
title: Control GROUPBOX (menús y otros recursos)
description: Define un control de cuadro de grupo. El control es un rectángulo que agrupa otros controles. Los controles se agrupan dibujando un borde alrededor de ellos y mostrando el texto especificado en la esquina superior izquierda.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menús de control GROUPBOX y otros recursos
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252398"
---
# <a name="groupbox-control"></a>Control GROUPBOX

Define un control de cuadro de grupo. El control es un rectángulo que agrupa otros controles. Los controles se agrupan dibujando un borde alrededor de ellos y mostrando el texto especificado en la esquina superior izquierda.

La **instrucción GROUPBOX,** que solo se puede usar en una instrucción [**DIALOGEX,**](dialogex-resource.md) define el texto, el identificador, las dimensiones y los atributos de una ventana de control.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación del estilo de clase de botón **BS \_ GROUPBOX** y los estilos **\_ WS TABSTOP** y **WS \_ DISABLED.**

Si no especifica un estilo, el estilo predeterminado es **BS \_ GROUPBOX**.

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="remarks"></a>Observaciones

Cuando el estilo contiene **WS \_ TABSTOP** o el texto especifica un acelerador, el tabulador o la tecla de aceleración mueve el foco al primer control dentro del grupo.

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de cuadro de grupo con la etiqueta Opciones:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Cuadros de grupo](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




