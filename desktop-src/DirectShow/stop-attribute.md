---
description: El atributo stop especifica la hora de detenerse de un objeto, en relación con el objeto primario.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: stop (Atributo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050180"
---
# <a name="stop-attribute"></a>stop (Atributo)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `stop` atributo especifica la hora de detenerse de un objeto, en relación con el objeto primario.

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *hh:mm:ss.ff,* donde *hh* = horas, *mm* = minutos, *ss* = segundos y *ff* = fracciones de segundos. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



