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
# <a name="sspi-handles"></a><span data-ttu-id="26fef-103">Identificadores SSPI</span><span class="sxs-lookup"><span data-stu-id="26fef-103">SSPI Handles</span></span>

<span data-ttu-id="26fef-104">SSPI usa los siguientes tipos de identificador y puntero a estos identificadores:</span><span class="sxs-lookup"><span data-stu-id="26fef-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="26fef-105">**SecHandle** y **PSecHandle**</span><span class="sxs-lookup"><span data-stu-id="26fef-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="26fef-106">**CredHandle** y **PCredHandle**</span><span class="sxs-lookup"><span data-stu-id="26fef-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="26fef-107">**CtxtHandle** y **PCtxtHandle**</span><span class="sxs-lookup"><span data-stu-id="26fef-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="26fef-108">Estos tipos de control y punteros a estos tipos de identificador se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="26fef-108">These handle types and pointers to these handle types are defined as follows.</span></span>


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



 

 



