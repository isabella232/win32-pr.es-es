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
# <a name="create-the-main-animation-objects"></a>Crear los objetos de animación principales

Para usar la animación de Windows en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.

## <a name="overview"></a>Información general

Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador de animaciones, el temporizador de animación y los objetos de la biblioteca de transición.

Estos objetos serán necesarios para crear y mostrar animaciones, por lo que normalmente no deben liberarse hasta que se cierre la aplicación. Si no hay ninguna posibilidad de que cualquier devolución de llamada registrada pudiera haber creado un ciclo de referencia, la liberación de los objetos es suficiente para una limpieza adecuada. De lo contrario, la aplicación se puede limpiar borrando las devoluciones de llamada (pasando **null** en el lugar de cada una) o llamando al método [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) del administrador de animaciones.

## <a name="example-code"></a>Código de ejemplo

El siguiente código de ejemplo se toma de MainWindow. cpp en los ejemplos de animación de Windows. Vea el método CMainWindow:: InitializeAnimation.


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



Tenga en cuenta las siguientes definiciones de MainWindow. h.


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



## <a name="next-step"></a>siguiente paso

Después de completar este paso, el paso siguiente es: [crear variables de animación](create-animation-variables.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Información general sobre animaciones de Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 