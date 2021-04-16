---
title: AmbientAttributes.accKeyboardShortcut
description: El atributo accKeyboardShortcut especifica o recupera una descripción del método abreviado de teclado para cualquier elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes. accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699547"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

El atributo **accKeyboardShortcut** especifica o recupera una descripción del método abreviado de teclado para cualquier elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura con un valor predeterminado de "" (cadena vacía). En el caso del elemento **Button** , este atributo tiene un valor predeterminado de "barra espaciadora o entrar". En el caso del elemento **Slider** , el valor predeterminado es "Right/up Arrow to Increment, Left/Down Arrow to reduce".

## <a name="remarks"></a>Observaciones

Este atributo se usa para fines de accesibilidad. Permite una descripción del método abreviado de teclado para que un programa lector lea en voz alta un elemento. Este atributo no establece el acceso directo. El scripter debe hacer ese trabajo.

Este atributo también se aplica a los elementos de botón dentro del control de grupo de botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





