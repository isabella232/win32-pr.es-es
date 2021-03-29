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
# <a name="ajax"></a><span data-ttu-id="78405-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="78405-103">AJAX</span></span>

<span data-ttu-id="78405-104">Las características de AJAX en Windows Internet Explorer 8 como [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) y [mensajería entre documentos (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) tienen propiedades nativas que pueden entrar en conflicto con las propiedades personalizadas existentes.</span><span class="sxs-lookup"><span data-stu-id="78405-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="78405-105">Windows Internet Explorer expone nuevas propiedades para ciertas características de AJAX, como [la mensajería entre documentos (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), incluso en la vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="78405-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="78405-106">Si agrega propiedades personalizadas al objeto de evento, podrían entrar en conflicto con estas nuevas propiedades, como el **origen**.</span><span class="sxs-lookup"><span data-stu-id="78405-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="78405-107">El siguiente ejemplo de código funciona en versiones anteriores de Internet Explorer, pero no en versiones más recientes porque las nuevas características utilizan la propiedad **source** .</span><span class="sxs-lookup"><span data-stu-id="78405-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="78405-108">En el ejemplo de código siguiente se muestra cómo se puede cambiar este objeto para que siga siendo compatible.</span><span class="sxs-lookup"><span data-stu-id="78405-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="78405-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78405-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78405-110">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="78405-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



