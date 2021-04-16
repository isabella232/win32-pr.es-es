---
description: Los contextos de activación son objetos con recuento de referencias. La aplicación debe tener una referencia en un contexto de activación para poder usarlo.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Recuento de referencias contextos de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649194"
---
# <a name="reference-counting-activation-contexts"></a>Recuento de referencias contextos de activación

Los contextos de activación son objetos con recuento de referencias. La aplicación debe tener una referencia en un contexto de activación para poder usarlo. Las funciones de la API de contexto de activación que toman un contexto de activación pueden realizar su propio recuento de referencias. Por ejemplo, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta y [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) disminuye el recuento de referencias. Sin embargo, si la aplicación pasa un contexto de activación sin usar estas funciones, la aplicación debe proporcionar su propio método de recuento de referencias.

Cuando una aplicación llama a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), el identificador devuelto tendrá un recuento de referencias de uno. Una vez que la aplicación finaliza con el contexto de activación, se debe liberar el identificador y reducir el recuento de referencias mediante una llamada a [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). No intente usar [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ni otras funciones de administración de memoria en el identificador del contexto de activación.

En el ejemplo siguiente se muestra un método para controlar el recuento de referencias a lo largo de la duración de un contexto de activación. La función FUNC crea un contexto de activación, que luego pasa al destino del objeto, que incrementa el recuento de referencias a 2. De hecho, el vuelve a liberar su referencia en el contexto de activación y reduce el recuento de referencias de nuevo a 1. A continuación, el destino posee su propia referencia cuando se llama de nuevo a SetActCtx o cuando se destruye el objeto.


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
