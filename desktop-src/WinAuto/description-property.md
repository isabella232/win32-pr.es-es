---
title: Propiedad Description (características de accesibilidad de Windows)
description: La propiedad Description de un objeto proporciona una descripción textual de la apariencia visual de un objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488872"
---
# <a name="description-property-windows-accessibility-features"></a>Propiedad Description (características de accesibilidad de Windows)

> [!Note]  
> La propiedad **Description** se suele usar incorrectamente y no es compatible con la automatización de la interfaz de usuario de Microsoft. Los desarrolladores de Microsoft Active Accessibility Server no deben usar esta propiedad. Si se necesita más información para escenarios de accesibilidad y automatización, use las propiedades admitidas por los elementos de UI Automation y los patrones de control.

 

La propiedad **Description** de un objeto proporciona una descripción textual de la apariencia visual de un objeto. La descripción se usa principalmente para proporcionar más contexto a los usuarios ciegos o de baja visión, pero también se usa para la búsqueda de contexto o para otras aplicaciones. Esta propiedad puede ayudar a los usuarios a entender un icono o la apariencia visual general.

La propiedad **Description** se recupera llamando a [**IAccessible:: get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Cuándo se debe admitir la propiedad Description

Los servidores admiten la propiedad **Description** si la descripción no es obvia, o cuando no es redundante en función del [**nombre**](name-property.md)del objeto, el [**rol**](role-property.md), el [**Estado**](state-property.md)y las propiedades de [**valor**](value-property.md) . Por ejemplo, un botón con la etiqueta "OK" no necesitaría información adicional, mientras que un botón que muestra una imagen de un cactus. Las propiedades **nombre**, **rol** y [**ayuda**](help-property.md) de este botón describen su finalidad, pero la propiedad **Descripción** transmite información que es menos tangible; por ejemplo, "este botón muestra una imagen de un cactus".

Un servidor de Microsoft Active Accessibility puede Agregar compatibilidad para la automatización de la interfaz de usuario mediante el uso de la [anotación directa](direct-annotation.md), el uso de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o la implementación de Microsoft Active Accessibility y la automatización de la interfaz de usuario en paralelo con las dos implementaciones que controlan el mensaje de la función [**\_ GETOBJECT de WM**](wm-getobject.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la anotación directa](using-direct-annotation.md)
</dt> <dt>

[La interfaz IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




