---
title: Leer los valores de las variables de animación
description: Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se animarán.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variables de animación Windows animación , lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242060"
---
# <a name="read-the-animation-variable-values"></a>Leer los valores de las variables de animación

Cada vez que la aplicación pinta, debe leer los valores actuales de las variables de animación que representan las características visuales que se animarán.

## <a name="overview"></a>Información general

Al dibujar un marco, una aplicación puede usar el método [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para solicitar los valores de las variables de animación que afectarán a los objetos visuales dentro del marco. Es posible recortar una variable de animación en un intervalo de valores [**(SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) y [**SetUpperBound)**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)y solicitar que su valor se redondee a un entero mediante un esquema de redondeo especificado ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).

En lugar de leer los valores de todas las variables para cada fotograma, una aplicación puede usar el método [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) para registrar uno o varios controladores de cambios de variables para recibir notificaciones solo cuando se cambia el valor de las variables ([**IUIAnimationVariableChangeHandler::OnValueChanged)**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)o un valor redondeado ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged).**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged) Para identificar las variables que se pasan a los controladores de cambios de variables, una aplicación puede aplicar etiquetas a las variables mediante el [**método IUIAnimationVariable::SetTag.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) Se trata de pares enteros de objeto (IUnknown) \* interpretados por la aplicación.

## <a name="example-code"></a>Código de ejemplo

El código de ejemplo siguiente se toma de Thumbnail.cpp en el Windows de cuadrícula de ejemplo [de animación](/windows/desktop/UIAnimation/grid-layout-sample); vea el método CMainWindow::Render. Usa el [**método GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) para leer los valores como valores de punto flotante.


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



El código de ejemplo siguiente se toma de MainWindow.cpp en la animación controlada por temporizador de Windows [ejemplo de animación](timer-driven-animation-sample.md); vea el método CMainWindow::D rawBackground. Usa el [**método GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para leer los valores como valores enteros.


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

Antes de iniciar este paso, debería haber completado este paso: Actualizar el Administrador de [animaciones y Dibujar fotogramas](introducing-windows-animation-manager.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el siguiente paso es: [Crear un guión gráfico y Agregar transiciones.](updating---timer-driven-animation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Windows Información general sobre animaciones](scenic-animation-api-overview.md)
</dt> </dl>

 

 