---
description: Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función InvalidateRect o InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidación y validación de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984950"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="61157-103">Invalidación y validación de la región de actualización</span><span class="sxs-lookup"><span data-stu-id="61157-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="61157-104">Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) .</span><span class="sxs-lookup"><span data-stu-id="61157-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="61157-105">Estas funciones agregan el rectángulo o región especificados (en coordenadas de cliente) a la región de actualización, combinando el rectángulo o la región con cualquier elemento que el sistema o la aplicación hayan agregado previamente a la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="61157-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="61157-106">Las funciones [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) y [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) no generan mensajes de [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="61157-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="61157-107">En su lugar, el sistema acumula los cambios realizados por estas funciones y sus propios cambios mientras una ventana procesa otros mensajes en su cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="61157-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="61157-108">Al acumular los cambios, una ventana procesa todos los cambios a la vez en lugar de actualizar bits y partes en un paso cada vez.</span><span class="sxs-lookup"><span data-stu-id="61157-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="61157-109">Las funciones [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) y [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validan una parte de la ventana quitando un rectángulo o una región especificados de la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="61157-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="61157-110">Estas funciones se utilizan normalmente cuando la ventana ha actualizado una parte específica de la pantalla en la región de actualización antes de recibir el mensaje de [**\_ dibujo de WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="61157-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 



