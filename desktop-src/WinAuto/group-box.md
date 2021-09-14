---
title: Group Box (Referencia del elemento de la interfaz de usuario de MSAA)
description: Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como casillas o botones de radio, y contiene un texto definido por la aplicación (etiqueta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358944"
---
# <a name="group-box-msaa-ui-element-reference"></a>Group Box (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos Group Box** para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **group box** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como casillas o botones de radio, y contiene un texto definido por la aplicación (etiqueta).

El único propósito de un cuadro de grupo es organizar los controles relacionados con un propósito común, indicado por la etiqueta .

El nombre de clase de ventana de un cuadro de grupo es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cuadro de grupo admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un cuadro de grupo admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** siempre es cero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Los cuadros de grupo no tienen métodos abreviados de teclado. Sin embargo, si el texto de la ventana del cuadro de grupo contiene un carácter de yerba (&), Microsoft Active Accessibility devuelve una cadena que no es NULL como la **propiedad KeyboardShortcut.**                                                                                                                                                                                                                                            |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad** Name se obtiene del texto de la ventana (o título) del control, que se muestra con el cuadro de grupo.                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad** Parent es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ GROUPING.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





