---
description: Se supone que todos los ejemplos de la documentación del SDK de Criptografía incluyen y \# \# definen directivas de compilador.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#incluye y #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774280"
---
# <a name="includes-and-defines"></a>\#incluye y \# define

Se supone que todos los ejemplos de la **\#** documentación del SDK de Criptografía incluyen y **\# definen** directivas de compilador.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Además, la **\_ constante \_ WINNT de WIN32** debe definirse correctamente. Para obtener más información sobre **\_ \_ WINNT de WIN32,** vea [Using the Windows Headers](../winprog/using-the-windows-headers.md).

 

 
