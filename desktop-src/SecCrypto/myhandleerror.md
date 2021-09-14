---
description: La función MyHandleError es un ejemplo de una función de herramienta que se usa para imprimir un mensaje de error y salir del programa que realiza la llamada.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047c9642a1b19c2af4a6e5ef2134ca305c472c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173186"
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



 

 



