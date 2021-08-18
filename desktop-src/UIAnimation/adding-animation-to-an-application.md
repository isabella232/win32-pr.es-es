---
title: Crear los objetos de animación principales
description: Para usar Windows animation en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- objetos de administrador de animación Windows animación ,creating
- objetos de temporizador de animación Windows animation ,creating
- objetos de biblioteca de transición Windows animación ,creating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3023e5934581850bb6aa21e7d41d92642bb01fadfcf7531fcacabca74b411f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137408"
---
# <a name="create-the-main-animation-objects"></a>Crear los objetos de animación principales

Para usar Windows animation en la aplicación, el primer paso es crear un pequeño conjunto de objetos de animación principales.

## <a name="overview"></a>Información general

Use la [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador de animaciones, el temporizador de animación y los objetos de la biblioteca de transición.

Estos objetos serán necesarios para crear y mostrar animaciones, por lo que normalmente no deben liberarse hasta que se cierre la aplicación. Si no hay ninguna posibilidad de que las devoluciones de llamada registradas puedan haber creado un ciclo de referencia, liberar los objetos es suficiente para una limpieza adecuada. De lo contrario, la aplicación puede limpiar borrando las devoluciones de llamada (pasando **NULL** en lugar de cada una) o llamando al método Shutdown del administrador [**de**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) animaciones.

## <a name="example-code"></a>Código de ejemplo

El código de ejemplo siguiente se toma de MainWindow.cpp en los ejemplos Windows animation; vea el método CMainWindow::InitializeAnimation.


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



Tenga en cuenta las siguientes definiciones de MainWindow.h.


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

Después de completar este paso, el siguiente paso es: Crear [variables de animación](create-animation-variables.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows Información general sobre animaciones](scenic-animation-api-overview.md)
</dt> </dl>

 

 