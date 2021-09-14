---
description: El atributo mstart especifica la hora de inicio de un clip, en relación con el archivo multimedia original.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Atributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062298"
---
# <a name="mstart-attribute"></a>Atributo mstart

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mstart` atributo especifica la hora de inicio de un clip, en relación con el archivo multimedia original.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *hh:mm:ss.ff,* donde *hh* = horas, *mm* = minutos, *ss* = segundos y *ff* = fracciones de segundos. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



