---
title: Eliminación de un objeto
description: Eliminación de un objeto
ms.assetid: 54ea1e7d-75b5-461f-b0d6-a976c33d66fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e94e55c025d3358f50170b83042b6e888622e14897d02607b9fc24ed0dea1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144538"
---
# <a name="deleting-an-object"></a>Eliminación de un objeto

El **método Release** elimina el objeto cuando su recuento de referencias es cero.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::Release() 
{ 
    if (!--m_refs) 
    { 
        delete this;   // If O, delete this instance. 
        return 0; 
    } 
    return m_refs; 
} 

```



 

 




