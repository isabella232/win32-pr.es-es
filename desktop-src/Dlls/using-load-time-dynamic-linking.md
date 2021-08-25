---
description: Después de crear un archivo DLL, puede usar las funciones que define en una aplicación. A continuación se muestra una sencilla aplicación de consola que usa la función myPuts exportada desde Myputs.dll (consulte Creación de una biblioteca de Dynamic-Link simple).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Uso Load-Time dynamic linking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106d9d73808b56c664e44d8dcd71b74a65431316fd3daf47dd0736596c5aa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902375"
---
# <a name="using-load-time-dynamic-linking"></a>Uso Load-Time dynamic linking

Después de crear un archivo DLL, puede usar las funciones que define en una aplicación. A continuación se muestra una sencilla aplicación de consola que usa la función myPuts exportada desde Myputs.dll (consulte Creación de una biblioteca [de Dynamic-Link simple).](creating-a-simple-dynamic-link-library.md)

Dado que en este ejemplo se llama explícitamente a la función DLL, el módulo de la aplicación debe vincularse a la biblioteca de importación Myputs.lib. Para obtener más información sobre la creación de archivos DLL, consulte la documentación incluida con las herramientas de desarrollo.


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

 

 



