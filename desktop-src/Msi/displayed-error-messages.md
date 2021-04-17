---
description: Una función de instalador puede mostrar un cuadro de diálogo de mensaje de error que devuelve cualquiera de los siguientes errores. Solo se muestra un cuadro de error si el nivel de la interfaz de usuario está en el nivel completo, reducido o básico. Para obtener más información, consulte niveles de la interfaz de usuario.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Mensajes de error mostrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652541"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="49c33-105">Mensajes de error mostrados</span><span class="sxs-lookup"><span data-stu-id="49c33-105">Displayed Error Messages</span></span>

<span data-ttu-id="49c33-106">Una [función de instalador](installer-function-reference.md) puede mostrar un cuadro de diálogo de mensaje de error que devuelve cualquiera de los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="49c33-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="49c33-107">Solo se muestra un cuadro de error si el nivel de la interfaz de usuario está en el nivel completo, reducido o básico.</span><span class="sxs-lookup"><span data-stu-id="49c33-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="49c33-108">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="49c33-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="49c33-109">Las funciones del instalador solo muestran mensajes de error que se encuentran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49c33-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="49c33-110">En el caso de los errores que no están en esta lista, el autor de la llamada de la función es responsable de controlar la presentación de los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="49c33-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="49c33-111">Código de error</span><span class="sxs-lookup"><span data-stu-id="49c33-111">Error code</span></span>               | <span data-ttu-id="49c33-112">Error</span><span class="sxs-lookup"><span data-stu-id="49c33-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="49c33-113">ERROR de \_ instalación de \_ suspensión</span><span class="sxs-lookup"><span data-stu-id="49c33-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="49c33-114">La instalación se suspendió.</span><span class="sxs-lookup"><span data-stu-id="49c33-114">The install was suspended.</span></span>   |
| <span data-ttu-id="49c33-115">ERROR al \_ instalar \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="49c33-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="49c33-116">El usuario salió de la instalación.</span><span class="sxs-lookup"><span data-stu-id="49c33-116">The user exited the install.</span></span> |
| <span data-ttu-id="49c33-117">ERROR de instalación de ERROR \_ \_</span><span class="sxs-lookup"><span data-stu-id="49c33-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="49c33-118">Error de instalación.</span><span class="sxs-lookup"><span data-stu-id="49c33-118">Install failed.</span></span>              |



 

 

 



