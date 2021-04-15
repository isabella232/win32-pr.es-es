---
title: Crear los objetos de animación principales
description: Para usar la animación de Windows en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- objetos del administrador de animaciones animación de Windows, crear
- objetos de temporizador de animación animación de Windows, crear
- objetos de biblioteca de transición animación de Windows, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421184"
---
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="7aa30-106">Crear los objetos de animación principales</span><span class="sxs-lookup"><span data-stu-id="7aa30-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="7aa30-107">Para usar la animación de Windows en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.</span><span class="sxs-lookup"><span data-stu-id="7aa30-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="7aa30-108">Información general</span><span class="sxs-lookup"><span data-stu-id="7aa30-108">Overview</span></span>

<span data-ttu-id="7aa30-109">Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador de animaciones, el temporizador de animación y los objetos de la biblioteca de transición.</span><span class="sxs-lookup"><span data-stu-id="7aa30-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="7aa30-110">Estos objetos serán necesarios para crear y mostrar animaciones, por lo que normalmente no deben liberarse hasta que se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7aa30-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="7aa30-111">Si no hay ninguna posibilidad de que cualquier devolución de llamada registrada pudiera haber creado un ciclo de referencia, la liberación de los objetos es suficiente para una limpieza adecuada.</span><span class="sxs-lookup"><span data-stu-id="7aa30-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="7aa30-112">De lo contrario, la aplicación se puede limpiar borrando las devoluciones de llamada (pasando **null** en el lugar de cada una) o llamando al método [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) del administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="7aa30-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="7aa30-113">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="7aa30-113">Example Code</span></span>

<span data-ttu-id="7aa30-114">El siguiente código de ejemplo se toma de MainWindow. cpp en los ejemplos de animación de Windows. Vea el método CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="7aa30-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



<span data-ttu-id="7aa30-115">Tenga en cuenta las siguientes definiciones de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="7aa30-115">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a><span data-ttu-id="7aa30-116">siguiente paso</span><span class="sxs-lookup"><span data-stu-id="7aa30-116">Next Step</span></span>

<span data-ttu-id="7aa30-117">Después de completar este paso, el paso siguiente es: [crear variables de animación](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="7aa30-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aa30-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7aa30-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aa30-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7aa30-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="7aa30-120">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="7aa30-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="7aa30-121">**IUIAnimationTimer**</span><span class="sxs-lookup"><span data-stu-id="7aa30-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="7aa30-122">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="7aa30-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="7aa30-123">Información general sobre animaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="7aa30-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 