---
description: Debido a la superficie de los archivos dll vinculados estáticamente, debe evitar el uso de Microsoft Foundation Classes (MFCs) para escribir un experto.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Usar Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815174"
---
# <a name="using-microsoft-foundation-classes"></a>Usar Microsoft Foundation Classes

Debido a la superficie de los archivos dll vinculados estáticamente, debe evitar el uso de Microsoft Foundation Classes (MFCs) para escribir un experto. Sin embargo, si utiliza MFC, asegúrese de tener acceso a cualquiera de los recursos DLL de MFC incluyendo el código siguiente inmediatamente después de la entrada:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



