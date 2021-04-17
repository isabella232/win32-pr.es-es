---
description: 'Hay tres funciones que generan cuadros de diálogo para controlar los errores: SetupCopyError, SetupDeleteError y SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Control de errores (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666647"
---
# <a name="error-handling-setup-api"></a>Control de errores (API de instalación)

Hay tres funciones que generan cuadros de diálogo para controlar los errores: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)y [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Las rutinas de devolución de llamada pueden usar estas funciones para generar una interfaz de usuario para controlar las notificaciones de [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)y [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .

Cada una de estas funciones de control de errores genera un cuadro de diálogo que pide al usuario información sobre cómo proceder. Al igual que con [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), puede modificar el diseño y el comportamiento del cuadro de diálogo especificando marcas durante la llamada de función.

 

 



