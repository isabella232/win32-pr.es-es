---
description: Se supone que todos los ejemplos de la documentación del SDK de criptografía tienen las siguientes \# directivas de \# compilador include y define.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#incluye y #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689643"
---
# <a name="includes-and-defines"></a><span data-ttu-id="ef78c-103">\#incluye y \# define</span><span class="sxs-lookup"><span data-stu-id="ef78c-103">\#includes and \#defines</span></span>

<span data-ttu-id="ef78c-104">Se supone que todos los ejemplos de la documentación del SDK de criptografía tienen las siguientes directivas de compilador **\# include** y **\# define** .</span><span class="sxs-lookup"><span data-stu-id="ef78c-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="ef78c-105">Además, la constante **\_ \_ WinNT de Win32** debe estar definida adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="ef78c-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="ef78c-106">Para obtener más información acerca de **\_ Win32 \_ WinNT**, vea [usar los encabezados de Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="ef78c-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
