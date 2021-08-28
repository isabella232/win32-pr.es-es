---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e683bb441642e8f9764ac0cfe8313d0aa0df92ae3276f986f5fdf6837d6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795925"
---
# <a name="ajax"></a>AJAX

Las características ajax de Windows Internet Explorer 8, como [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) y la mensajería entre documentos [(XDM),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) tienen propiedades nativas que podrían estar en conflicto con las propiedades personalizadas existentes.

Windows Internet Explorer expone nuevas propiedades para determinadas características de AJAX, como la mensajería entre documentos [(XDM),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)incluso en Vista de compatibilidad. Si agrega propiedades personalizadas al objeto de evento, podrían estar en conflicto con estas nuevas propiedades, como **el origen**.

El ejemplo de código siguiente funciona en versiones anteriores de Internet Explorer pero no en versiones más recientes porque las nuevas características usan la **propiedad de** origen.


```JScript
event.source = myObject;
```



En el ejemplo de código siguiente se muestra cómo puede cambiar este objeto para que siga siendo compatible.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



