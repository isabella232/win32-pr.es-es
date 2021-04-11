---
description: Las funciones GetUpdateRect y GetUpdateRgn recuperan la región de actualización actual para la ventana.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recuperación de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275978"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="0b51e-103">Recuperación de la región de actualización</span><span class="sxs-lookup"><span data-stu-id="0b51e-103">Retrieving the Update Region</span></span>

<span data-ttu-id="0b51e-104">Las funciones [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) y [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperan la región de actualización actual para la ventana.</span><span class="sxs-lookup"><span data-stu-id="0b51e-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="0b51e-105">GetUpdateRect recupera el rectángulo más pequeño (en coordenadas lógicas) que incluye toda la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="0b51e-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="0b51e-106">GetUpdateRgn recupera la propia región de actualización.</span><span class="sxs-lookup"><span data-stu-id="0b51e-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="0b51e-107">Estas funciones se pueden usar para calcular el tamaño actual de la región de actualización con el fin de determinar dónde realizar una operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="0b51e-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="0b51e-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) también recupera las dimensiones del rectángulo más pequeño que rodea la región de actualización actual y copia las dimensiones en el miembro **rcPaint** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="0b51e-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="0b51e-109">Dado que **BeginPaint** valida la región de actualización, cualquier llamada a [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) y [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) inmediatamente después de una llamada a **BeginPaint** devuelve una región de actualización vacía.</span><span class="sxs-lookup"><span data-stu-id="0b51e-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



