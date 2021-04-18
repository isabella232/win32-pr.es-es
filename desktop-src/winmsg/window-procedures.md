---
description: En esta sección se describen los procedimientos de ventana. Cada ventana tiene un procedimiento de ventana asociado que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707130"
---
# <a name="window-procedures"></a><span data-ttu-id="10caf-104">Procedimientos de ventana</span><span class="sxs-lookup"><span data-stu-id="10caf-104">Window Procedures</span></span>

<span data-ttu-id="10caf-105">Cada ventana tiene un procedimiento de ventana asociado, una función que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase.</span><span class="sxs-lookup"><span data-stu-id="10caf-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="10caf-106">Todos los aspectos de la apariencia y el comportamiento de una ventana dependen de la respuesta del procedimiento de ventana a estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="10caf-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="10caf-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="10caf-107">In This Section</span></span>



| <span data-ttu-id="10caf-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="10caf-108">Name</span></span>                                                         | <span data-ttu-id="10caf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="10caf-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10caf-110">Acerca de los procedimientos de ventana</span><span class="sxs-lookup"><span data-stu-id="10caf-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="10caf-111">Describe los procedimientos de ventana.</span><span class="sxs-lookup"><span data-stu-id="10caf-111">Discusses window procedures.</span></span> <span data-ttu-id="10caf-112">Cada ventana es miembro de una clase de ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="10caf-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="10caf-113">La clase Window determina el procedimiento de ventana predeterminado que usa una ventana individual para procesar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="10caf-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="10caf-114">Usar procedimientos de ventana</span><span class="sxs-lookup"><span data-stu-id="10caf-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="10caf-115">Explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana.</span><span class="sxs-lookup"><span data-stu-id="10caf-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="10caf-116">Referencia de procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="10caf-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="10caf-117">Contiene la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="10caf-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="10caf-118">Functions</span><span class="sxs-lookup"><span data-stu-id="10caf-118">Functions</span></span>



| <span data-ttu-id="10caf-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="10caf-119">Name</span></span>                                     | <span data-ttu-id="10caf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="10caf-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10caf-121">**CallWindowProc**</span><span class="sxs-lookup"><span data-stu-id="10caf-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="10caf-122">Pasa información del mensaje al procedimiento de ventana especificado.</span><span class="sxs-lookup"><span data-stu-id="10caf-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="10caf-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="10caf-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="10caf-124">Llama al procedimiento de ventana predeterminado para proporcionar el procesamiento predeterminado de los mensajes de ventana que una aplicación no procesa.</span><span class="sxs-lookup"><span data-stu-id="10caf-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="10caf-125">Esta función garantiza que se procesan todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="10caf-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="10caf-126">Se llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) con los mismos parámetros recibidos por el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="10caf-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="10caf-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10caf-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="10caf-128">Función definida por la aplicación que procesa los mensajes enviados a una ventana.</span><span class="sxs-lookup"><span data-stu-id="10caf-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="10caf-129">El tipo **WndProc** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="10caf-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="10caf-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10caf-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
