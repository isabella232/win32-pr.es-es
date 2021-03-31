---
description: Los componentes bien creados no alterar el entorno de la aplicación de hospedaje ni pierden contextos de activación.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Aislar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907835"
---
# <a name="isolating-components"></a><span data-ttu-id="2077b-103">Aislar componentes</span><span class="sxs-lookup"><span data-stu-id="2077b-103">Isolating Components</span></span>

<span data-ttu-id="2077b-104">Los componentes bien creados no alterar el entorno de la aplicación de hospedaje ni pierden contextos de activación.</span><span class="sxs-lookup"><span data-stu-id="2077b-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="2077b-105">Los componentes bien creados realizan su propia administración de contexto en lugar de depender del entorno de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2077b-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="2077b-106">El autor del componente hospedado está en la mejor posición para saber exactamente qué otros ensamblados requiere el componente.</span><span class="sxs-lookup"><span data-stu-id="2077b-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="2077b-107">Confiar en la aplicación host para proporcionar el entorno correcto para el componente hospedado es una causa probable de errores.</span><span class="sxs-lookup"><span data-stu-id="2077b-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="2077b-108">En su lugar, cree un manifiesto para el componente hospedado que especifique todas sus dependencias y, a continuación, compile con reconocimiento de aislamiento \_ \_ habilitado.</span><span class="sxs-lookup"><span data-stu-id="2077b-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="2077b-109">Esto garantiza que las llamadas externas realizadas por el componente estén aisladas y usen las versiones correctas.</span><span class="sxs-lookup"><span data-stu-id="2077b-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="2077b-110">Dado que el contexto de activación \_ que \_ usa el reconocimiento de aislamiento habilitado es por dll, es seguro usarlo en varios archivos dll, cada uno con su propio manifiesto que llama a las dependencias.</span><span class="sxs-lookup"><span data-stu-id="2077b-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="2077b-111">Si no es posible compilar con reconocimiento de aislamiento \_ \_ habilitado, use una solución como la que se presenta en [usar devoluciones de llamada de componentes hospedados](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="2077b-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="2077b-112">Debe activar su propio contexto de activación en todos los puntos de entrada a los que puede llamar la aplicación de hospedaje para asegurarse de que el componente hospedado se ejecuta completamente con el contexto de activación correcto.</span><span class="sxs-lookup"><span data-stu-id="2077b-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="2077b-113">Puede utilizar un objeto auxiliar de C++ para facilitar el cambio de todos los entryPoints.</span><span class="sxs-lookup"><span data-stu-id="2077b-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="2077b-114">Por ejemplo, podría utilizar una clase de C++ como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2077b-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="2077b-115">A continuación, se puede usar en el componente mediante una variable global para almacenar el contexto de activación que se debe activar en cada punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="2077b-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="2077b-116">De esta manera, puede aislar el componente de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2077b-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



