---
title: Asignación de una unidad a un recurso compartido
description: En el ejemplo siguiente se muestra cómo conectar una letra de unidad a un recurso compartido de servidor remoto con una llamada a la función WNetAddConnection2. El ejemplo informa al usuario de si la llamada se realizó correctamente o no.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cb4c930250f74cc549d9b5a31f121b92abad0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421057"
---
# <a name="assigning-a-drive-to-a-share"></a>Asignación de una unidad a un recurso compartido

En el ejemplo siguiente se muestra cómo conectar una letra de unidad a un recurso compartido de servidor remoto con una llamada a la función [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) . El ejemplo informa al usuario de si la llamada se realizó correctamente o no.

Para probar el siguiente ejemplo de código, realice los pasos siguientes:

1.  Cambie las líneas siguientes a cadenas válidas:

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Agregue el archivo a una aplicación de consola denominada AddConn2.
3.  Vincule el MPR de la biblioteca. LIB a la lista de bibliotecas del compilador.
4.  Compile y ejecute el programa AddConn2.EXE.


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 