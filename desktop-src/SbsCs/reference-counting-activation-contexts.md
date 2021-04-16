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
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="d636f-104">Recuento de referencias contextos de activación</span><span class="sxs-lookup"><span data-stu-id="d636f-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="d636f-105">Los contextos de activación son objetos con recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d636f-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="d636f-106">La aplicación debe tener una referencia en un contexto de activación para poder usarlo.</span><span class="sxs-lookup"><span data-stu-id="d636f-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="d636f-107">Las funciones de la API de contexto de activación que toman un contexto de activación pueden realizar su propio recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d636f-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="d636f-108">Por ejemplo, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta y [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) disminuye el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d636f-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="d636f-109">Sin embargo, si la aplicación pasa un contexto de activación sin usar estas funciones, la aplicación debe proporcionar su propio método de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d636f-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="d636f-110">Cuando una aplicación llama a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), el identificador devuelto tendrá un recuento de referencias de uno.</span><span class="sxs-lookup"><span data-stu-id="d636f-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="d636f-111">Una vez que la aplicación finaliza con el contexto de activación, se debe liberar el identificador y reducir el recuento de referencias mediante una llamada a [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span><span class="sxs-lookup"><span data-stu-id="d636f-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="d636f-112">No intente usar [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ni otras funciones de administración de memoria en el identificador del contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="d636f-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="d636f-113">En el ejemplo siguiente se muestra un método para controlar el recuento de referencias a lo largo de la duración de un contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="d636f-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="d636f-114">La función FUNC crea un contexto de activación, que luego pasa al destino del objeto, que incrementa el recuento de referencias a 2.</span><span class="sxs-lookup"><span data-stu-id="d636f-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="d636f-115">De hecho, el vuelve a liberar su referencia en el contexto de activación y reduce el recuento de referencias de nuevo a 1.</span><span class="sxs-lookup"><span data-stu-id="d636f-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="d636f-116">A continuación, el destino posee su propia referencia cuando se llama de nuevo a SetActCtx o cuando se destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="d636f-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


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



 

 
