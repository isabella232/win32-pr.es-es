---
title: Leer los valores de las variables de animación
description: Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variables de animación animación de Windows, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695690"
---
# <a name="read-the-animation-variable-values"></a>Leer los valores de las variables de animación

Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se van a animar.

## <a name="overview"></a>Información general

Al dibujar un marco, una aplicación puede usar el método [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable:: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para solicitar los valores de cualquier variable de animación que afecte a los objetos visuales del marco. Es posible recortar una variable de animación a un intervalo de valores ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) y solicitar que su valor se redondee a un entero mediante un esquema de redondeo especificado ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).

En lugar de leer los valores de todas las variables de cada fotograma, una aplicación puede usar el método [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) para registrar uno o más controladores de cambios de variable para recibir notificaciones solo cuando se produce un cambio en el valor de las variables ([**IUIAnimationVariableChangeHandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) o un valor redondeado ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)). Para identificar las variables que se pasan a los controladores de cambios de variable, una aplicación puede aplicar etiquetas a las variables mediante el método [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) . Estos son objetos (IUnknown \* ), pares de enteros que se interpretan por la aplicación.

## <a name="example-code"></a>Código de ejemplo

El siguiente código de ejemplo se toma de thumbnail. cpp en el diseño de [cuadrícula](/windows/desktop/UIAnimation/grid-layout-sample)de ejemplo de animación de Windows. Vea el método CMainWindow:: Render. Usa el método [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) para leer los valores como valores de punto flotante.


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow::D rawBackground. Usa el método [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para leer los valores como valores enteros.


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a>Paso anterior

Antes de comenzar este paso, debe haber completado este paso: [actualizar el administrador de animaciones y dibujar Marcos](introducing-windows-animation-manager.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el paso siguiente es [crear un guión gráfico y agregar transiciones](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Información general sobre animaciones de Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 