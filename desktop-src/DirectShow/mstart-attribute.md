---
description: El atributo mstart especifica la hora de inicio de un clip, en relación con el archivo multimedia original.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Atributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050955"
---
# <a name="mstart-attribute"></a>Atributo mstart

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mstart` atributo especifica la hora de inicio de un clip, en relación con el archivo multimedia original.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *hh:mm:ss.ff,* donde *hh* = hours, *mm* = minutes, *ss* = seconds y *ff* = fractions of seconds. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



