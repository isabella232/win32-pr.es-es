---
title: Comprobar el estado de un parámetro de accesibilidad
description: En el fragmento de código siguiente se usa la función GetSystemMetrics para comprobar el parámetro ShowSounds. Si GetSystemMetrics devuelve TRUE, la aplicación debe presentar toda la información importante en el formulario visual.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077843"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a><span data-ttu-id="846df-104">Comprobar el estado de un parámetro de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="846df-104">Checking the State of an Accessibility Parameter</span></span>

<span data-ttu-id="846df-105">En el fragmento de código siguiente se usa la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para comprobar el parámetro ShowSounds.</span><span class="sxs-lookup"><span data-stu-id="846df-105">The following code fragment uses the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to check the ShowSounds parameter.</span></span> <span data-ttu-id="846df-106">Si **GetSystemMetrics** devuelve **true**, la aplicación debe presentar toda la información importante en el formulario visual.</span><span class="sxs-lookup"><span data-stu-id="846df-106">If **GetSystemMetrics** returns **TRUE**, the application should present all important information in visual form.</span></span>


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 