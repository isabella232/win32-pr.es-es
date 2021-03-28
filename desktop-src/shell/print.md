---
description: La API de Shell proporciona funciones que se pueden usar para administrar impresoras en red. Si un archivo tiene asociado el verbo imprimir, puede usar el comando ShellExecuteEx para imprimirlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Administrar impresoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985638"
---
# <a name="managing-printers"></a>Administrar impresoras

La API de Shell proporciona funciones que se pueden usar para administrar impresoras en red. Si un archivo tiene asociado el verbo **Imprimir** , puede usar el comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimirlo.

-   [Administración de impresoras](#printer-management)
-   [Imprimir archivos con ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Administración de impresoras

Puede administrar impresoras en un sistema con la función [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) . Esta función le permite:

-   Instalar impresoras.
-   Abra impresoras.
-   Obtiene las propiedades de la impresora.
-   Crear vínculos de impresora.
-   Imprima una página de prueba.

## <a name="printing-files-with-shellexecuteex"></a>Imprimir archivos con ShellExecuteEx

Si un tipo de archivo tiene un comando de impresión asociado, puede imprimir el archivo llamando a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con **Print** como el verbo. Este comando suele ser el mismo que el utilizado para el verbo **abierto** , con la adición de una marca para indicar a la aplicación que imprima el archivo. Por ejemplo, Microsoft WordPad puede imprimir archivos. txt. El verbo **Open** de un archivo. txt se correspondería a algo como el comando siguiente:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Cuando se usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir un archivo. txt, WordPad abre el archivo, lo imprime y, a continuación, lo cierra, y devuelve el control a la aplicación. La siguiente función de ejemplo toma una ruta de acceso completa y usa **ShellExecuteEx** para imprimirla, mediante el comando Print asociado a su extensión de nombre de archivo.


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



 

 



