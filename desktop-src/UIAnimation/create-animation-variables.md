---
title: Crear variables de animación
description: Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- variables de animación animación de Windows, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421225"
---
# <a name="create-animation-variables"></a>Crear variables de animación

Una aplicación debe crear una variable de animación para cada característica de visual que se va a animar mediante la animación de Windows.

## <a name="overview"></a>Información general

Las variables de animación se crean mediante el administrador de animaciones y la aplicación debe conservar una referencia a cada para siempre que sea necesario. Normalmente, la aplicación creará cada variable de animación al mismo tiempo que el objeto visual que anima.

Cuando se crea una variable de animación, se debe especificar su valor inicial. Después, su valor solo puede modificarse mediante la programación de guiones gráficos que lo animan.

Las variables de animación se pasan como parámetros cuando se construyen guiones gráficos, por lo que la aplicación no debe liberarlas hasta que no sea necesario animar las características visuales que representan, normalmente cuando los objetos visuales asociados están a punto de ser destruidos.

## <a name="example-code"></a>Código de ejemplo

-   [Animar colores](#animating-colors)
-   [Animar coordenadas x e y](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animar colores

El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplos de animaciones [controladas](application-driven-animation-sample.md) por la aplicación y la [animación controlada por temporizador](timer-driven-animation-sample.md). En el ejemplo, se crean tres variables de animación mediante [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) para representar los colores de fondo. El código también usa los métodos [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) para controlar el valor de la variable de animación.


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



Tenga en cuenta las siguientes definiciones de MainWindow. h.


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

El siguiente código de ejemplo se toma de thumbnail. cpp en el [ejemplo de diseño de cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample)de animación de Windows. Vea el método CMainWindow:: CreateAnimationVariables. Se crean dos variables de animación para representar las coordenadas X e y de cada objeto.


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



Tenga en cuenta las siguientes definiciones de thumbnail. h.


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



Las variables de animación son números de punto flotante, pero sus valores también se pueden capturar como enteros. De forma predeterminada, cada valor se redondea al entero más próximo, pero es posible invalidar el modo de redondeo que se usa para una variable. En el ejemplo de código siguiente se usa el método [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) para especificar que los valores siempre se deben redondear hacia abajo.


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

Antes de comenzar este paso, debe haber completado este paso: [crear los objetos de animación principales](adding-animation-to-an-application.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el paso siguiente es [actualizar el administrador de animaciones y dibujar fotogramas](introducing-windows-animation-manager.md).

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

[Información general sobre animaciones de Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 