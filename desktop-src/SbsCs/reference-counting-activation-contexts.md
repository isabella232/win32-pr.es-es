---
description: Los contextos de activación son objetos con recuento de referencias. La aplicación debe tener una referencia en un contexto de activación para poder usarla.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Contextos de activación de recuento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141938"
---
# <a name="reference-counting-activation-contexts"></a>Contextos de activación de recuento de referencias

Los contextos de activación son objetos con recuento de referencias. La aplicación debe tener una referencia en un contexto de activación para poder usarla. Las funciones de activation Context API que toman un contexto de activación pueden realizar su propio recuento de referencias. Por ejemplo, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta y [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) reduce el recuento de referencias. Sin embargo, si la aplicación pasa un contexto de activación sin usar estas funciones, la aplicación debe proporcionar su propio método de recuento de referencias.

Cuando una aplicación llama a [**CreateActCtx,**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)el identificador devuelto tendrá un recuento de referencias de uno. Una vez que la aplicación finaliza con el contexto de activación, se debe liberar el identificador y reducir el recuento de referencias mediante una llamada [**a ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). No intente usar [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ni ninguna otra función de administración de memoria en el identificador de contexto de activación.

En el ejemplo siguiente se muestra un método para controlar el recuento de referencias a lo largo de la duración de un contexto de activación. La función Funct crea un contexto de activación, que luego pasa al objeto Target, que incrementa el recuento de referencias a 2. A continuación, Funct libera su referencia en el contexto de activación y reduce el recuento de referencias a 1. Después, el destino posee la liberación de su propia referencia cuando se vuelve a llamar a SetActCtx o cuando se destruye el objeto.


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



 

 
