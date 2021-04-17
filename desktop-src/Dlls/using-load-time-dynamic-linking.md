---
description: Después de crear un archivo DLL, puede utilizar las funciones que define en una aplicación. A continuación se muestra una sencilla aplicación de consola que usa la función allocas exportada desde Myputs.dll (consulte Creación de una biblioteca de Dynamic-Link sencilla).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Usar Load-Time vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666845"
---
# <a name="using-load-time-dynamic-linking"></a>Usar Load-Time vinculación dinámica

Después de crear un archivo DLL, puede utilizar las funciones que define en una aplicación. A continuación se muestra una sencilla aplicación de consola que usa la función allocas exportada desde Myputs.dll (consulte [creación de una biblioteca de Dynamic-Link sencilla](creating-a-simple-dynamic-link-library.md)).

Dado que en este ejemplo se llama a la función DLL explícitamente, el módulo de la aplicación debe vincularse a la biblioteca de importación. lib. Para obtener más información acerca de la compilación de archivos dll, consulte la documentación que se incluye con las herramientas de desarrollo.


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación dinámica en tiempo de carga](load-time-dynamic-linking.md)
</dt> </dl>

 

 



