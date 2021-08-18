---
title: Propiedad Description (Windows de accesibilidad)
description: La propiedad Description de un objeto proporciona una descripción textual sobre la apariencia visual de un objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994235"
---
# <a name="description-property-windows-accessibility-features"></a>Propiedad Description (Windows de accesibilidad)

> [!Note]  
> La **propiedad** Description a menudo se usa incorrectamente y no es compatible con Microsoft Automatización de la interfaz de usuario. Microsoft Active Accessibility desarrolladores de servidores no deben usar esta propiedad. Si se necesita más información para escenarios de accesibilidad y automatización, use las propiedades admitidas por Automatización de la interfaz de usuario elementos y patrones de control.

 

La propiedad **Description** de un objeto proporciona una descripción textual sobre la apariencia visual de un objeto. La descripción se usa principalmente para proporcionar un contexto mayor para usuarios con visión baja o invidentes, pero también se usa para la búsqueda de contexto u otras aplicaciones. Esta propiedad puede ayudar a los usuarios a comprender un icono o la apariencia visual general.

La **propiedad Description** se recupera mediante una llamada a [**IAccessible::get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Cuándo admitir la propiedad Description

Los servidores admiten la propiedad **Description** si la descripción no es obvia o cuando no es redundante en función de las propiedades [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md)y [**Value del**](value-property.md) objeto. Por ejemplo, un botón con la etiqueta "Ok" (Aceptar) no necesitará información adicional, mientras que un botón que muestre una imagen de un vídeo lo haría. Las **propiedades Name**, **Role** y [**Help**](help-property.md) de este tipo de botón describen su propósito, pero la propiedad **Description** transmite información menos tangible; por ejemplo, "Este botón muestra una imagen de un archivo".

Un servidor Microsoft Active Accessibility puede agregar compatibilidad con Automatización de la interfaz de usuario mediante anotación directa [,](direct-annotation.md)mediante la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) o implementando Microsoft Active Accessibility y Automatización de la interfaz de usuario en paralelo con ambas implementaciones que controlen el [**mensaje \_ GETOBJECT de WM.**](wm-getobject.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar anotación directa](using-direct-annotation.md)
</dt> <dt>

[Interfaz IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




