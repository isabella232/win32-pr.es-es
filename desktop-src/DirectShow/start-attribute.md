---
description: El atributo start especifica la hora de inicio de un objeto, en relación con el objeto primario.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: atributo start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227b04a8cd7dc366a9cf10a4930233cd834e2bea7faa64bb59c248049b9e9abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650995"
---
# <a name="start-attribute"></a>atributo start

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `start` atributo especifica la hora de inicio de un objeto, en relación con el objeto primario.

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

 

 



