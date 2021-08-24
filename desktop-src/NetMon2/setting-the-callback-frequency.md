---
description: Use el código siguiente para establecer la frecuencia de devolución de llamada.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Establecer la frecuencia de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363251"
---
# <a name="setting-the-callback-frequency"></a>Establecer la frecuencia de devolución de llamada

Use el código siguiente para establecer la frecuencia de devolución de llamada:

**DWORD** Valor = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Este fragmento de código establece la frecuencia de devolución de llamada en 1 segundo (el valor mínimo). El valor máximo debe ser mucho mayor que 1. Si el búfer del proveedor de paquetes de red (NPP) está lleno, el NPP llama al monitor antes.

 

 



