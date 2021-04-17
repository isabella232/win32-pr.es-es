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
# <a name="error-handling-setup-api"></a><span data-ttu-id="97c07-103">Control de errores (API de instalación)</span><span class="sxs-lookup"><span data-stu-id="97c07-103">Error Handling (Setup API)</span></span>

<span data-ttu-id="97c07-104">Hay tres funciones que generan cuadros de diálogo para controlar los errores: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)y [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span><span class="sxs-lookup"><span data-stu-id="97c07-104">There are three functions that generate dialog boxes to handle errors: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), and [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span>

<span data-ttu-id="97c07-105">Las rutinas de devolución de llamada pueden usar estas funciones para generar una interfaz de usuario para controlar las notificaciones de [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)y [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .</span><span class="sxs-lookup"><span data-stu-id="97c07-105">Callback routines can use these functions to generate a user interface to handle [**SPFILENOTIFY\_COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md), and [**SPFILENOTIFY\_RENAMEERROR**](spfilenotify-renameerror.md) notifications.</span></span>

<span data-ttu-id="97c07-106">Cada una de estas funciones de control de errores genera un cuadro de diálogo que pide al usuario información sobre cómo proceder.</span><span class="sxs-lookup"><span data-stu-id="97c07-106">Each of these error-handling functions generates a dialog box that asks the user for information on how to proceed.</span></span> <span data-ttu-id="97c07-107">Al igual que con [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), puede modificar el diseño y el comportamiento del cuadro de diálogo especificando marcas durante la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="97c07-107">As with [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), you can modify the dialog box's layout and behavior by specifying flags during the function call.</span></span>

 

 



