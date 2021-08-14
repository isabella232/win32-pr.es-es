---
description: Debido a la superficie de archivos DLL vinculados estáticamente, debe evitar el uso de Microsoft Foundation Classes (MFC) para escribir un experto.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Uso de Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362934"
---
# <a name="using-microsoft-foundation-classes"></a>Uso de Microsoft Foundation Classes

Debido a la superficie de archivos DLL vinculados estáticamente, debe evitar el uso de Microsoft Foundation Classes (MFC) para escribir un experto. Sin embargo, si usa MFC, asegúrese de tener acceso a cualquiera de los recursos dll de MFC mediante la inclusión del código siguiente inmediatamente después de la entrada:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



