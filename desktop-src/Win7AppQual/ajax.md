---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003018"
---
# <a name="ajax"></a>AJAX

Las características de AJAX en Windows Internet Explorer 8 como [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) y [mensajería entre documentos (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) tienen propiedades nativas que pueden entrar en conflicto con las propiedades personalizadas existentes.

Windows Internet Explorer expone nuevas propiedades para ciertas características de AJAX, como [la mensajería entre documentos (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), incluso en la vista de compatibilidad. Si agrega propiedades personalizadas al objeto de evento, podrían entrar en conflicto con estas nuevas propiedades, como el **origen**.

El siguiente ejemplo de código funciona en versiones anteriores de Internet Explorer, pero no en versiones más recientes porque las nuevas características utilizan la propiedad **source** .


```JScript
event.source = myObject;
```



En el ejemplo de código siguiente se muestra cómo se puede cambiar este objeto para que siga siendo compatible.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



