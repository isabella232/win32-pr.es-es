---
title: Comprobar el estado de un parámetro de accesibilidad
description: El fragmento de código siguiente usa la función GetSystemMetrics para comprobar el parámetro Show Sounds. Si GetSystemMetrics devuelve TRUE, la aplicación debe presentar toda la información importante en formato visual.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122255"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Comprobar el estado de un parámetro de accesibilidad

El fragmento de código siguiente usa [**la función GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para comprobar el parámetro ShowSounds. Si **GetSystemMetrics** devuelve **TRUE,** la aplicación debe presentar toda la información importante en formato visual.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 