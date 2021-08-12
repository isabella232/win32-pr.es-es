---
description: El atributo userdata especifica los datos persistentes definidos por la aplicación para un objeto .
ms.assetid: 7f1390be-93d4-440f-8b46-57a6a3e0e2a1
title: atributo userdata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f25b9293781fe89618e7e0db7359f8a7bfbc002f2c2a057314827bdf876262b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651209"
---
# <a name="userdata-attribute"></a>atributo userdata

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `userdata` atributo especifica los datos persistentes definidos por la aplicación para un objeto .

## <a name="possible-values"></a>Valores posibles

El valor debe ser un número hexadecimal con un número par de dígitos. Los valores A-F deben estar en mayúsculas. No use un prefijo como 0x. Ejemplo: 123ABC.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetUserData**](iamtimelineobj-setuserdata.md)
</dt> </dl>

 

 



