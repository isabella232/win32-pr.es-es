---
title: Crear variables de animación
description: Una aplicación debe crear una variable de animación para cada característica visual que se va a animar mediante Windows Animación.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- variables de animación Windows animation ,creating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb81e2f94f987ad6b9c923083c76565fa75b2cc665753233c8a84b6eb1a1d52a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008235"
---
# <a name="create-animation-variables"></a>Crear variables de animación

Una aplicación debe crear una variable de animación para cada característica visual que se va a animar mediante Windows Animación.

## <a name="overview"></a>Información general

Las variables de animación se crean mediante el administrador de animaciones y la aplicación debe conservar una referencia a cada una de ellas mientras sea necesario. Por lo general, la aplicación creará cada variable de animación al mismo tiempo que el objeto visual que anima.

Cuando se crea una variable de animación, se debe especificar su valor inicial. A partir de entonces, su valor solo se puede modificar programando guiones gráficos que lo animan.

Las variables de animación se pasan como parámetros cuando se construyen guiones gráficos, por lo que la aplicación no debe liberarlas hasta que las características visuales que representan ya no necesiten animarse, normalmente cuando los objetos visuales asociados están a punto de destruirse.

## <a name="example-code"></a>Código de ejemplo

-   [Animar colores](#animating-colors)
-   [Animar coordenadas x e y](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animar colores

El código de ejemplo siguiente se toma de MainWindow.cpp en los ejemplos Windows Animación controlada por la aplicación y Animación [controlada por temporizador](timer-driven-animation-sample.md). [](application-driven-animation-sample.md) En el ejemplo, se crean tres variables de animación [**mediante CreateAnimationVariable para**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) representar los colores de fondo. El código también usa los [**métodos SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) para controlar el valor de la variable de animación.


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



Tenga en cuenta las siguientes definiciones de MainWindow.h.


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a>Animar coordenadas x e y

El código de ejemplo siguiente se toma de Thumbnail.cpp en el ejemplo Windows diseño de cuadrícula [de animación](/windows/desktop/UIAnimation/grid-layout-sample); vea el método CMainWindow::CreateAnimationVariables. Se crean dos variables de animación para representar las coordenadas X e Y de cada objeto.


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



Tenga en cuenta las siguientes definiciones de Thumbnail.h.


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



Las variables de animación son números de punto flotante, pero sus valores también se pueden capturar como enteros. De forma predeterminada, cada valor se redondeará al entero más cercano, pero es posible invalidar el modo de redondeo utilizado para una variable. En el código de ejemplo siguiente se [**usa el método SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) para especificar que los valores siempre se deben redondear hacia abajo.


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a>Paso anterior

Antes de iniciar este paso, debería haber completado este paso: [Crear los objetos de animación principales](adding-animation-to-an-application.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el siguiente paso es: Actualizar el Administrador de [animaciones y Dibujar fotogramas](introducing-windows-animation-manager.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**IUIAnimationVariable::SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**IUIAnimationVariable::SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**IUIAnimationVariable::SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Windows Información general sobre animaciones](scenic-animation-api-overview.md)
</dt> </dl>

 

 