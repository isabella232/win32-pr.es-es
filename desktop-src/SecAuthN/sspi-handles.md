---
description: Enumera los identificadores usados por la API de SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Identificadores SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160972"
---
# <a name="sspi-handles"></a>Identificadores SSPI

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



 

 



