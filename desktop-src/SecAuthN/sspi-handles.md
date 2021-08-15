---
description: Enumera los identificadores usados por la API de SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Identificadores de SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fadebea7ff6b32f0058106595718a24d589854a662ef7b504ce6d7e8e5bc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916974"
---
# <a name="sspi-handles"></a>Identificadores de SSPI

SSPI usa los siguientes tipos de identificador y puntero a estos identificadores:

-   **SecHandle** y **PSecHandle**
-   **CredHandle** y **PCredHandle**
-   **CtxtHandle** y **PCtxtHandle**

Estos tipos de identificador y punteros a estos tipos de identificador se definen de la manera siguiente.


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



 

 



