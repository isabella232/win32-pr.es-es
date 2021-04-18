---
description: Use los controles estándar de Windows siempre que sea posible, ya que son totalmente compatibles con las directrices de Microsoft Active Accessibility. Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca de controles comunes de Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Usar controles estándar de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360256"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="748c1-104">Usar controles estándar de Windows</span><span class="sxs-lookup"><span data-stu-id="748c1-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="748c1-105">Use los controles estándar de Windows siempre que sea posible, ya que son totalmente compatibles con las directrices de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="748c1-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="748c1-106">Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca de controles comunes de Windows (Comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="748c1-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="748c1-107">Cada control estándar de Windows es una ventana independiente de una clase específica, por lo que se notifica a la ayuda de accesibilidad cuando el foco se mueve a un nuevo control.</span><span class="sxs-lookup"><span data-stu-id="748c1-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="748c1-108">La ayuda puede determinar la clase de ventana controles y los mensajes adicionales que puede enviar para consultar o modificar el estado de los controles.</span><span class="sxs-lookup"><span data-stu-id="748c1-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="748c1-109">La ayuda también puede identificar todos los controles secundarios incluidos en una ventana primaria e identificar el elemento primario de cualquier control.</span><span class="sxs-lookup"><span data-stu-id="748c1-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="748c1-110">Algunos controles comunes son extremadamente flexibles y a menudo pueden sustituirse por controles personalizados y controles dibujados por el propietario menos accesibles.</span><span class="sxs-lookup"><span data-stu-id="748c1-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="748c1-111">Por ejemplo, una vista de lista puede reemplazar un cuadro de lista dibujado por el propietario para mostrar una casilla junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="748c1-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="748c1-112">Como otro ejemplo, el control de botón mejorado puede mostrar imágenes y texto.</span><span class="sxs-lookup"><span data-stu-id="748c1-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="748c1-113">Anteriormente, esto requería el uso de un control personalizado.</span><span class="sxs-lookup"><span data-stu-id="748c1-113">Previously, this required the use of a custom control.</span></span>

 

 



