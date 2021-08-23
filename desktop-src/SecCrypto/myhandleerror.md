---
description: La función MyHandleError es un ejemplo de una función de herramienta que se usa para imprimir un mensaje de error y salir del programa que realiza la llamada.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a3c3ad412b6719b59402e820411377c08d2c6b9a17f44771a7156e0b52567a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739665"
---
# <a name="myhandleerror"></a>MyHandleError

La **función MyHandleError** es un ejemplo de una función de herramienta que se usa para imprimir un mensaje de error y salir del programa que realiza la llamada. Los ejemplos de varias funciones De CryptoAPI en [Referencia de criptografía](cryptography-reference.md) y los ejemplos más extendidos en Uso de [criptografía](using-cryptography.md) implementan esta función. Las aplicaciones reales pueden requerir una funcionalidad de control de errores más compleja.


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

```



 

 



