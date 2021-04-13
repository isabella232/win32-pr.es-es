---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487691"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="11167-103">IAgentEx::ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="11167-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="11167-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11167-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="11167-105">Muestra la ventana Propiedades de carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="11167-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="11167-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="11167-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="11167-107"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="11167-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="11167-108">Coordenada x de la ventana en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="11167-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="11167-109"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="11167-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="11167-110">Coordenada y de la ventana en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="11167-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="11167-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span><span class="sxs-lookup"><span data-stu-id="11167-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="11167-112">Marca de posición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="11167-112">Default position flag.</span></span> <span data-ttu-id="11167-113">Si este parámetro es **true**, el agente de Microsoft muestra la ventana de la hoja de propiedades para el carácter predeterminado en la última ubicación que aparecía.</span><span class="sxs-lookup"><span data-stu-id="11167-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="11167-114">En Windows 2000, puede que sea necesario llamar a la nueva API de [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) para asegurarse de que esta ventana se convierte en la ventana de primer plano.</span><span class="sxs-lookup"><span data-stu-id="11167-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="11167-115">Para obtener más información sobre cómo establecer la ventana de primer plano en Windows 2000, vea la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="11167-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="11167-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11167-116">See Also</span></span>

[<span data-ttu-id="11167-117">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="11167-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 