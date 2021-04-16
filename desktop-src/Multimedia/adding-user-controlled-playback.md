---
title: Agregar User-Controlled reproducción
description: Agregar User-Controlled reproducción
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651300"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="fa2ed-104">Agregar User-Controlled reproducción</span><span class="sxs-lookup"><span data-stu-id="fa2ed-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="fa2ed-105">Puede Agregar la reproducción controlada por el usuario a una aplicación existente llamando a la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fa2ed-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="fa2ed-106">Los parámetros de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifican los identificadores de la ventana primaria y la instancia de módulo asociada a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="fa2ed-107">También especifican los estilos de ventana y el nombre de archivo (o nombre de dispositivo) que se asociarán a la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="fa2ed-108">**MCIWndCreate** realiza automáticamente los pasos siguientes que, para otras clases de ventana, implementaría en el código usted mismo:</span><span class="sxs-lookup"><span data-stu-id="fa2ed-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="fa2ed-109">Registre la clase de ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="fa2ed-110">Cree la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="fa2ed-111">Cargar el contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-111">Load the specified content.</span></span>
4.  <span data-ttu-id="fa2ed-112">Establecer la posición de reproducción actual al principio del contenido.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="fa2ed-113">Muestra el control de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-113">Display the device control.</span></span>
6.  <span data-ttu-id="fa2ed-114">Muestra el área de reproducción de la ventana, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-114">Display the playback area of the window, if needed.</span></span>

 

 




