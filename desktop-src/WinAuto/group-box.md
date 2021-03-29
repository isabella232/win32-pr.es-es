---
title: Cuadro de grupo (referencia de elementos de interfaz de usuario de MSAA)
description: Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como las casillas o los botones de radio, y contiene un texto definido por la aplicación (etiqueta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778108"
---
# <a name="group-box-msaa-ui-element-reference"></a>Cuadro de grupo (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **cuadro de grupo** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **cuadro de grupo** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como las casillas o los botones de radio, y contiene un texto definido por la aplicación (etiqueta).

El único propósito de un cuadro de grupo es organizar los controles relacionados con un propósito común, indicado por la etiqueta.

El nombre de clase de ventana de un cuadro de grupo es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cuadro de grupo admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un cuadro de grupo admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** siempre es cero.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Los cuadros de grupo no tienen métodos abreviados de teclado. Sin embargo, si el texto de la ventana del cuadro de grupo contiene un carácter de y comercial (&), Microsoft Active Accessibility devuelve una cadena que no es NULL como la propiedad **KeyboardShortcut** .                                                                                                                                                                                                                                            |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** se obtiene del texto (o título) de la ventana del control, que se muestra con el cuadro de grupo.                                                                                                                                                                                                                                                                                                                                                    |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                              |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**la \_ \_ agrupación del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                            |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





