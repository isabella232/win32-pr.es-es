---
title: Active Accessibility y Automatización de la interfaz de usuario
description: Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fa4c06d528281552c47b987a07fba416376b3291f40315770ed98be944554e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071915"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility y Automatización de la interfaz de usuario

Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores. Los desarrolladores de controles personalizados y aplicaciones cliente de tecnología accesibles para Windows XP y Windows Vista deben considerar el uso de Microsoft Automatización de la interfaz de usuario en [su lugar.](entry-uiauto-win32.md)

Microsoft Automatización de la interfaz de usuario es un sistema completo que proporciona información más precisa sobre la interfaz de usuario y ofrece al usuario más capacidad de interactuar con los controles. En concreto, proporciona compatibilidad mejorada para texto.

Un conjunto de objetos proxy proporciona Automatización de la interfaz de usuario para controles estándar de Microsoft Win32 y Windows Forms. La compatibilidad más enriquecte está disponible para los controles escritos específicamente con Automatización de la interfaz de usuario en mente, incluidos los elementos Windows Presentation Foundation nativos (WPF), que no admiten directamente Microsoft Active Accessibility. Los controles personalizados que admiten Automatización de la interfaz de usuario pueden escribirse en código administrado o no administrado.

Microsoft Active Accessibility clientes tienen acceso limitado, a través de una capa de puente, a elementos de interfaz de usuario que solo admiten Automatización de la interfaz de usuario. Para obtener más información, [vea Apéndice G: Active Accessibility Bridge to Automatización de la interfaz de usuario](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Para obtener más información sobre las similitudes y diferencias entre Microsoft Active Accessibility y Automatización de la interfaz de usuario, vea Microsoft Active Accessibility [y Automatización de la interfaz de usuario Compared](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Automatización de la interfaz de usuario](entry-uiauto-win32.md)
</dt> </dl>

 

 




