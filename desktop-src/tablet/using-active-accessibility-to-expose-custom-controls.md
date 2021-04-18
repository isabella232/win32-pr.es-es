---
description: Descripción del uso de Active Accessibility para exponer controles personalizados para Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usar Active Accessibility para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705546"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Usar Active Accessibility para exponer controles personalizados

Puede usar Microsoft Active Accessibility como una forma eficaz de que los controles personalizados sean compatibles con las ayudas de accesibilidad. Active Accessibility requiere que la aplicación:

-   Cree objetos de modelo de objetos componentes (COM) que representen controles personalizados individuales o grupos de controles que admitan correctamente la interfaz **IAccessible** . (El objeto puede crearse a petición cuando lo solicite un cliente de Active Accessibility).
-   Llame a [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) cuando se crean o destruyen los controles, se obtiene o se pierde el foco o se cambia el estado.
-   Controlar el \_ mensaje de la GETOBJECT de WM cuando se utiliza para consultar las propiedades del objeto u objetos.

Para los fines de este debate, una ventana que contenga otros objetos personalizados también debe exponerse a Active Accessibility, lo que permite al cliente detectar y navegar a los objetos secundarios. Para obtener más información sobre cómo hacer que los controles personalizados sean compatibles con las ayudas de accesibilidad, vea [accesibilidad](../accessibility/accessibility.md).

 

 
