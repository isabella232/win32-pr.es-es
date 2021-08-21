---
description: Shell API proporciona funciones que puede usar para administrar impresoras en red. Si un archivo tiene asociado el verbo de impresión, puede usar el comando ShellExecuteEx para imprimirlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Administración de impresoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7086b360355d0ad85be440bc8bc9e330bfa6dd25793cc943d3aacdbaa0d4a8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719603"
---
# <a name="managing-printers"></a>Administración de impresoras

Shell API proporciona funciones que puede usar para administrar impresoras en red. Si un archivo tiene asociado **el** verbo de impresión, puede usar el [**comando ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimirlo.

-   [Administración de impresoras](#printer-management)
-   [Impresión de archivos con ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Administración de impresoras

Puede administrar impresoras en un sistema con la [**función SHInvokePrinterCommand.**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) Esta función le permite:

-   Instale impresoras.
-   Abra impresoras.
-   Obtiene las propiedades de la impresora.
-   Cree vínculos de impresora.
-   Imprima una página de prueba.

## <a name="printing-files-with-shellexecuteex"></a>Impresión de archivos con ShellExecuteEx

Si un tipo de archivo tiene un comando de impresión asociado, puede imprimir el archivo llamando a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con **print** como verbo. Este comando suele ser el mismo que el que se usa para el **verbo** abierto, con la adición de una marca para que la aplicación imprima el archivo. Por ejemplo, .txt archivos se pueden imprimir mediante Microsoft WordPad. El **verbo** abierto para un .txt archivo se correspondería con algo parecido al comando siguiente:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Cuando se usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir un archivo .txt, WordPad abre el archivo, lo imprime y, a continuación, se cierra, devolviendo el control a la aplicación. La siguiente función de ejemplo toma una ruta de acceso completa y usa **ShellExecuteEx** para imprimirla, mediante el comando print asociado a su extensión de nombre de archivo.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



