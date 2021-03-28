---
description: El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en minimizar en el menú ventana o la aplicación llama a la función ShowWindow y especifica un valor como SW \_ minimizar.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Ventanas minimizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811935"
---
# <a name="minimized-windows"></a><span data-ttu-id="48c49-103">Ventanas minimizadas</span><span class="sxs-lookup"><span data-stu-id="48c49-103">Minimized Windows</span></span>

<span data-ttu-id="48c49-104">El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en minimizar en el menú ventana o la aplicación llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) y especifica un valor como SW \_ minimizar.</span><span class="sxs-lookup"><span data-stu-id="48c49-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="48c49-105">Minimizar una ventana acelera el rendimiento del sistema reduciendo la cantidad de trabajo que debe realizar una aplicación al actualizar su ventana principal.</span><span class="sxs-lookup"><span data-stu-id="48c49-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="48c49-106">En el caso de una aplicación típica, el sistema dibuja un icono, denominado icono de clase, cuando se minimiza la ventana, etiquetando el icono con el nombre de la ventana.</span><span class="sxs-lookup"><span data-stu-id="48c49-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="48c49-107">La aplicación especifica el icono de clase, una imagen estática que representa la aplicación, cuando registra la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="48c49-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="48c49-108">La aplicación asigna un identificador al icono de clase al miembro **hIcon** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) antes de llamar a [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="48c49-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="48c49-109">La aplicación puede usar la función [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar el identificador de icono.</span><span class="sxs-lookup"><span data-stu-id="48c49-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
