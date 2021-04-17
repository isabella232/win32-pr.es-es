---
description: El atributo UserData especifica los datos persistentes definidos por la aplicación para un objeto.
ms.assetid: 7f1390be-93d4-440f-8b46-57a6a3e0e2a1
title: UserData (atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4828e378bcdafddbf83b3676e0941c8a1a066cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687866"
---
# <a name="userdata-attribute"></a>UserData (atributo)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `userdata` atributo especifica los datos persistentes definidos por la aplicación para un objeto.

## <a name="possible-values"></a>Valores posibles

El valor debe ser un número de hexadecimal con un número par de dígitos. Los valores A – F deben escribirse en mayúsculas. No use un prefijo como 0x. Ejemplo: 123ABC.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md), [**transición**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetUserData**](iamtimelineobj-setuserdata.md)
</dt> </dl>

 

 



