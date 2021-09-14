---
description: Descripción del uso de accesibilidad activa para exponer controles personalizados para tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usar Active Accessibility para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361002"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Usar Active Accessibility para exponer controles personalizados

Puede usar Microsoft Active Accessibility una manera eficaz de hacer que los controles personalizados sean compatibles con las ayuda de accesibilidad. Active Accessibility requiere que la aplicación:

-   Cree objetos del Modelo de objetos componentes (COM) que representen controles personalizados individuales o grupos de controles que admitan correctamente la **interfaz IAccessible.** (El objeto se puede crear a petición cuando lo solicita un Active Accessibility cliente).
-   Llame [**a NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) cuando los controles se crean o destruyen, obtienen o pierden el foco o cambian de estado de otro modo.
-   Controle el mensaje GETOBJECT de WM \_ cuando se usa para consultar las propiedades del objeto u objetos.

Para esta explicación, también es necesario exponer en Active Accessibility una ventana que contenga otros objetos personalizados, lo que permite al cliente detectar y navegar a los objetos secundarios. Para obtener más información sobre cómo hacer que los controles personalizados sean compatibles con las ayuda de accesibilidad, vea [Accesibilidad.](../accessibility/accessibility.md)

 

 
