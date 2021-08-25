---
description: Descripción del uso de la accesibilidad activa para exponer controles personalizados para tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usar Active Accessibility para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d275b6c5639dddfe60f358427751ad4ff4cd7989923dc4a368b3316b3bfc01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934325"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Usar Active Accessibility para exponer controles personalizados

Puede usar Microsoft Active Accessibility una manera eficaz de hacer que los controles personalizados sean compatibles con las ayuda de accesibilidad. Active Accessibility requiere que la aplicación:

-   Cree objetos del Modelo de objetos componentes (COM) que representen controles personalizados individuales o grupos de controles que admitan correctamente la **interfaz IAccessible.** (El objeto se puede crear a petición cuando lo solicita un Active Accessibility cliente).
-   Llame [**a NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) cuando se crean o destruyen los controles, obtienen o pierden el foco o cambian de estado.
-   Controle el mensaje \_ WM GETOBJECT cuando se usa para consultar las propiedades del objeto u objetos.

Para los fines de esta explicación, una ventana que contiene otros objetos personalizados también debe exponerse a Active Accessibility, lo que permite al cliente detectar y navegar a los objetos secundarios. Para obtener más información sobre cómo hacer que los controles personalizados sean compatibles con las ayuda de accesibilidad, vea [Accesibilidad](../accessibility/accessibility.md).

 

 
