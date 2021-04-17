---
title: Active Accessibility y automatización de la interfaz de usuario
description: Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704787"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility y automatización de la interfaz de usuario

Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores. Los desarrolladores de controles personalizados y aplicaciones cliente de tecnología accesible para Windows XP y Windows Vista deben considerar el uso de la automatización de la [interfaz de usuario](entry-uiauto-win32.md) de Microsoft en su lugar.

La automatización de la interfaz de usuario de Microsoft es un sistema con todas las características que proporciona información más precisa sobre la interfaz de usuario y proporciona al usuario más capacidad para interactuar con los controles. En concreto, proporciona compatibilidad mejorada con el texto.

Un conjunto de objetos proxy proporciona compatibilidad con la automatización de la interfaz de usuario para los controles estándar de Microsoft Win32 y Windows Forms. La compatibilidad más enriquecida está disponible para los controles que se escriben específicamente con automatización de la interfaz de usuario, incluidos los elementos de Windows Presentation Foundation nativa (WPF), que no admiten directamente Microsoft Active Accessibility. Los controles personalizados que admiten la automatización de la interfaz de usuario se pueden escribir en código administrado o no administrado.

Los clientes de Microsoft Active Accessibility tienen acceso limitado, a través de una capa de puente, a elementos de interfaz de usuario que solo admiten la automatización de la interfaz de usuario. Para obtener más información, vea el [Apéndice G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Para obtener más información sobre las similitudes y diferencias entre Microsoft Active Accessibility y la automatización de la interfaz de usuario, consulte [comparación de microsoft Active Accessibility y UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Automatización de la interfaz de usuario](entry-uiauto-win32.md)
</dt> </dl>

 

 




