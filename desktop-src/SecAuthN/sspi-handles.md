---
description: Enumera los identificadores utilizados por la API SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Identificadores SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668253"
---
# <a name="sspi-handles"></a>Identificadores SSPI

SSPI usa los siguientes tipos de identificador y puntero a estos identificadores:

-   **SecHandle** y **PSecHandle**
-   **CredHandle** y **PCredHandle**
-   **CtxtHandle** y **PCtxtHandle**

Estos tipos de control y punteros a estos tipos de identificador se definen como se indica a continuación.


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



