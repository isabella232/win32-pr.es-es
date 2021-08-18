---
description: Este artículo contiene información sobre la administración de referencias de subprocesos mediante funciones de las funciones de utilidad ligera de Shell.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Administración de referencias de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6380957f5f8ef9be62e291820fe12d715f31a5f5bb5ba81b80aa1c8606478e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968924"
---
# <a name="managing-thread-references"></a>Administración de referencias de subprocesos

Este artículo contiene información sobre la administración de referencias de subprocesos mediante funciones de las funciones de utilidad ligera de Shell.


Surgen situaciones en las que un subproceso primario debe mantenerse activo durante la vigencia de un subproceso secundario. Por ejemplo, si se crea un objeto De modelo de objetos componentes (COM) en el subproceso primario y se serializa al subproceso secundario, ese subproceso primario no puede finalizar antes que el subproceso secundario. Para ello, shell proporciona estas funciones.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Use estas funciones en el subproceso primario como se describe aquí.

1.  Declare un procedimiento de subproceso definido por la aplicación siguiendo el formato de la [*función ThreadProc.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  En [*ThreadProc,*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))llame a [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) para crear una referencia al subproceso. Esto proporciona un puntero a una instancia de [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Este **IUnknown** usa el valor al que apunta *pcRef* para mantener un recuento de referencias. Siempre que este recuento sea mayor que 0, el subproceso permanece activo.
3.  Con ese puntero a [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)llame a [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) en [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). Esto establece la referencia para que las llamadas posteriores a [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) tengan algo que recuperar.
4.  Si [*threadProc crea*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) otro subproceso, *threadproc* de ese subproceso puede llamar a [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) con el puntero a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenido por [**SHCreateThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) Esto incrementa el recuento de referencias al que apunta el *parámetro pcRef* **en SHCreateThreadRef.**
5.  Cree el subproceso. Esto se hace normalmente mediante una llamada a [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), pasando un puntero a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) en el *parámetro pfnThreadProc.* Pase también la marca CTF \_ THREAD REF en el parámetro \_ *dwFlags.* El subproceso está activo siempre que *ThreadProc* se esté ejecutando.
6.  Cuando se crea un subproceso secundario, pase la marca **\_ CTF REF \_ COUNTED** en el parámetro *dwFlags* en la llamada a [**su SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  A medida que los subprocesos secundarios se completan y se liberan, disminuye el valor al que apunta *el elemento pcRef* del subproceso primario. Una vez completados todos los subprocesos secundarios, [*threadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) original puede completarse y liberar la referencia final del subproceso, quitando el recuento de referencias a 0. En ese momento, se libera la referencia al subproceso original abierto por [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) y se completa el subproceso.

Otra función relacionada es [**SHReleaseThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref) ThreadProc llama a [](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) esta función si el subproceso se ha creado mediante [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) con la **marca CTF \_ THREAD \_ REF.** Sin embargo, *ThreadProc* no es necesario para hacerlo implícitamente. Es [**necesario llamar a IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtenido a través de [**SHCreateThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)

 

 
