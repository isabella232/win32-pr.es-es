---
description: El atributo de punto de corte especifica cuándo se corta una transición de un origen al siguiente, si la transición se representa como un corte. El valor es relativo al inicio de la transición.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: atributo de punto de corte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654596"
---
# <a name="cutpoint-attribute"></a>atributo de punto de corte

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El atributo especifica cuándo se corta una transición de un origen al siguiente, si la transición `cutpoint` se representa como un corte. El valor es relativo al inicio de la transición.

## <a name="possible-values"></a>Valores posibles

Debe ser una cadena con el formato *hh:mm:ss.ff,* donde *hh* = horas, *mm* = minutos, *ss* = segundos y *ff* = fracciones de segundos. Ejemplo: 1:04:30.512. Se pueden omitir las unidades iniciales. Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.

## <a name="applies-to"></a>Se aplica a

[**Transición**](transition-element.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



