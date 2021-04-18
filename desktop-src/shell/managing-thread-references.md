---
description: Este artículo contiene información sobre la administración de las referencias de subprocesos mediante funciones de las funciones de utilidad de Shell ligero.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Administrar referencias de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985655"
---
# <a name="managing-thread-references"></a>Administrar referencias de subprocesos

Este artículo contiene información sobre la administración de las referencias de subprocesos mediante funciones de las funciones de utilidad de Shell ligero.


Surgen situaciones en las que un subproceso primario debe mantenerse activo mientras dure un subproceso secundario. Por ejemplo, si se crea un objeto de modelo de objetos componentes (COM) en el subproceso primario y se calculan las referencias al subproceso secundario, ese subproceso primario no puede finalizar antes del subproceso secundario. Para ello, el Shell proporciona estas funciones.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Use estas funciones en el subproceso primario como se describe aquí.

1.  Declare un procedimiento de subproceso definido por la aplicación según la forma de la función [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) .

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  En [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)), llame a [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) para crear una referencia al subproceso. Esto proporciona un puntero a una instancia de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Este **IUnknown** usa el valor al que apunta *pcRef* para mantener un recuento de referencias. Siempre que este recuento sea mayor que 0, el subproceso permanece activo.
3.  Con ese puntero a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), llame a [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) en [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). Esto establece la referencia para que las llamadas subsiguientes a [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) tengan algo que recuperar.
4.  Si su [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) crea otro subproceso, *ThreadProc* del subproceso puede llamar a [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) con el puntero a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenido por [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref). Esto incrementa el recuento de referencias al que apunta el parámetro *pcRef* en **SHCreateThreadRef**.
5.  Cree el subproceso. Esto se suele hacer llamando a [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), pasando un puntero a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) en el parámetro *pfnThreadProc* . También se pasa la \_ marca de referencia del subproceso CTF \_ en el parámetro *dwFlags* . El subproceso está activo siempre que se ejecute *ThreadProc* .
6.  Cuando se crea un subproceso secundario, pase la marca de **\_ \_ recuento de referencia de CTF** en el parámetro *dwFlags* en la llamada a su [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  A medida que se completan los subprocesos secundarios y se liberan, se reduce el valor al que apunta el *pcRef* del subproceso primario. Una vez completados todos los subprocesos secundarios, el valor de [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) original puede completarse y liberar la referencia de subproceso final, quitando el recuento de referencias a 0. En ese momento, se libera la referencia al subproceso original abierto por [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) y el subproceso se completa.

Otra función relacionada es [**SHReleaseThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref). [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) llama a esta función si el subproceso se ha creado con [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) con la marca **de \_ \_ referencia de subproceso CTF** . Sin embargo, no es necesario que *ThreadProc* lo haga implícitamente. Llamar a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenido a través de [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) es todo lo que hay que hacer.

 

 
