---
description: 'Hay tres funciones que generan cuadros de diálogo para controlar los errores: SetupCopyError, SetupDeleteError y SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Control de errores (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f3c69a4ab4943589d00354c401b1f35aa984b04552ecd03a1c4863fcf9134a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665995"
---
# <a name="error-handling-setup-api"></a>Control de errores (API de instalación)

Hay tres funciones que generan cuadros de diálogo para controlar los errores: [**SetupCopyError,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)y [**SetupRenameError.**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)

Las rutinas de devolución de llamada pueden usar estas funciones para generar una interfaz de usuario para controlar las notificaciones [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)y [**SPFILENOTIFY \_ RENAMEERROR.**](spfilenotify-renameerror.md)

Cada una de estas funciones de control de errores genera un cuadro de diálogo que solicita al usuario información sobre cómo continuar. Al igual [**que con SetupPromptForDisk,**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)puede modificar el diseño y el comportamiento del cuadro de diálogo especificando marcas durante la llamada de función.

 

 



