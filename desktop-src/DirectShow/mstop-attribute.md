---
description: El atributo mstop especifica el tiempo de detenerse de un clip, en relación con el archivo multimedia original.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Atributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072949"
---
# <a name="mstop-attribute"></a>Atributo mstop

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `mstop` atributo especifica el tiempo de detenerse de un clip, en relación con el archivo multimedia original.

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

 

 



