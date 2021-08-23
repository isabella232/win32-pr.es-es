---
description: Si este bit se establece en una casilla o un grupo de botones de radio, el botón se dibuja con la apariencia de un botón de inserción, pero su lógica permanece igual. Si no se establece el bit, los controles se dibujan en su estilo habitual.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Atributo de control PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692485"
---
# <a name="pushlike-control-attribute"></a>Atributo de control PushLike

Si este bit se establece en una casilla o un grupo de botones de radio, el botón se dibuja con la apariencia de un botón de inserción, pero su lógica permanece igual. Si no se establece el bit, los controles se dibujan en su estilo habitual.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit PushLike en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



