---
title: Interfaces de transición
description: Esta sección contiene las especificaciones de referencia para las interfaces Windows Animation Manager que admiten transiciones.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418605"
---
# <a name="transition-interfaces"></a>Interfaces de transición

Esta sección contiene las especificaciones de referencia para las interfaces Windows Animation Manager que admiten transiciones.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                     | Descripción                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Define métodos para crear un interpolador personalizado.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Extiende la interfaz [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) que define métodos para crear un interpolador personalizado. [**IUIAnimationInterpolator2 admite**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) la interpolación en una dimensión determinada. <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Define un método que permite que un interpolador personalizado proporcione información de transición, en forma de una curva polinómica cúbica, al administrador de animaciones.<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Define una transición, que determina cómo cambia una variable de animación con el tiempo.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Extiende la interfaz [**IUIAnimationTransition que**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) define una transición. Una [**transición IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) determina cómo cambia una variable de animación con el tiempo en una dimensión determinada.<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Define un método para crear transiciones desde interpoladores personalizados.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Define un método para crear transiciones desde interpoladores personalizados.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Define una biblioteca de transiciones estándar. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Define una biblioteca de transiciones estándar para una dimensión especificada.<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Define una variable de animación, que representa un elemento visual que se puede animar.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Define una variable de animación, que representa un elemento visual que se puede animar en varias dimensiones.<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Define un método para controlar eventos relacionados con las actualizaciones de variables de animación.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Define un método para controlar eventos de actualización de variables de animación. [**IUIAnimationVariableChangeHandler2 controla**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) los eventos que se producen en una dimensión especificada.<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Define un método para controlar eventos de actualización de variables de animación.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Define un método para controlar eventos de actualización de variables de animación. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) controla los eventos que se producen en una dimensión especificada.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Define un método para controlar eventos de actualización de curva de animación. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](windows-animation-reference.md)
</dt> </dl>

 

 





