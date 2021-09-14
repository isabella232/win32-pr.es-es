---
title: AmbientAttributes.accKeyboardShortcut
description: El atributo accKeyboardShortcut especifica o recupera una descripción de método abreviado de teclado para cualquier elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes.accKeyboardShortcut Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890052"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

El **atributo accKeyboardShortcut** especifica o recupera una descripción de método abreviado de teclado para cualquier elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura con un valor predeterminado de "" (cadena vacía). Para el **elemento BUTTON,** este atributo tiene un valor predeterminado de "Barra espaciadora o Entrar". Para el **elemento SLIDER,** el valor predeterminado es "Right/Up Arrow to increase, Left/Down Arrow to decrease".

## <a name="remarks"></a>Observaciones

Este atributo se usa con fines de accesibilidad. Permite que un programa de lector lea en voz alta una descripción del método abreviado de teclado para cualquier elemento. Este atributo no establece el acceso directo. El scripter debe hacer ese trabajo.

Este atributo también se aplica a los elementos de botón dentro del control de grupo de botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





