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
# <a name="isolating-components"></a>Aislar componentes

Los componentes bien creados no alterar el entorno de la aplicación de hospedaje ni pierden contextos de activación. Los componentes bien creados realizan su propia administración de contexto en lugar de depender del entorno de la aplicación de hospedaje.

El autor del componente hospedado está en la mejor posición para saber exactamente qué otros ensamblados requiere el componente. Confiar en la aplicación host para proporcionar el entorno correcto para el componente hospedado es una causa probable de errores. En su lugar, cree un manifiesto para el componente hospedado que especifique todas sus dependencias y, a continuación, compile con reconocimiento de aislamiento \_ \_ habilitado. Esto garantiza que las llamadas externas realizadas por el componente estén aisladas y usen las versiones correctas. Dado que el contexto de activación \_ que \_ usa el reconocimiento de aislamiento habilitado es por dll, es seguro usarlo en varios archivos dll, cada uno con su propio manifiesto que llama a las dependencias.

Si no es posible compilar con reconocimiento de aislamiento \_ \_ habilitado, use una solución como la que se presenta en [usar devoluciones de llamada de componentes hospedados](using-callbacks-from-hosted-components.md).

Debe activar su propio contexto de activación en todos los puntos de entrada a los que puede llamar la aplicación de hospedaje para asegurarse de que el componente hospedado se ejecuta completamente con el contexto de activación correcto. Puede utilizar un objeto auxiliar de C++ para facilitar el cambio de todos los entryPoints. Por ejemplo, podría utilizar una clase de C++ como la siguiente:


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



A continuación, se puede usar en el componente mediante una variable global para almacenar el contexto de activación que se debe activar en cada punto de entrada. De esta manera, puede aislar el componente de la aplicación de hospedaje.


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



 

 



