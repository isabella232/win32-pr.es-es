---
description: Descripción del uso de Active Accessibility para exponer controles personalizados para Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Usar Active Accessibility para exponer controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705546"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="61dae-103">Usar Active Accessibility para exponer controles personalizados</span><span class="sxs-lookup"><span data-stu-id="61dae-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="61dae-104">Puede usar Microsoft Active Accessibility como una forma eficaz de que los controles personalizados sean compatibles con las ayudas de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="61dae-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="61dae-105">Active Accessibility requiere que la aplicación:</span><span class="sxs-lookup"><span data-stu-id="61dae-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="61dae-106">Cree objetos de modelo de objetos componentes (COM) que representen controles personalizados individuales o grupos de controles que admitan correctamente la interfaz **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="61dae-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="61dae-107">(El objeto puede crearse a petición cuando lo solicite un cliente de Active Accessibility).</span><span class="sxs-lookup"><span data-stu-id="61dae-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="61dae-108">Llame a [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) cuando se crean o destruyen los controles, se obtiene o se pierde el foco o se cambia el estado.</span><span class="sxs-lookup"><span data-stu-id="61dae-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="61dae-109">Controlar el \_ mensaje de la GETOBJECT de WM cuando se utiliza para consultar las propiedades del objeto u objetos.</span><span class="sxs-lookup"><span data-stu-id="61dae-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="61dae-110">Para los fines de este debate, una ventana que contenga otros objetos personalizados también debe exponerse a Active Accessibility, lo que permite al cliente detectar y navegar a los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="61dae-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="61dae-111">Para obtener más información sobre cómo hacer que los controles personalizados sean compatibles con las ayudas de accesibilidad, vea [accesibilidad](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="61dae-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
