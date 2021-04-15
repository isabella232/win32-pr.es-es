---
title: Cómo implementar la información sobre herramientas para los iconos de la barra de estado
description: Una manera no intrusiva de mostrar un mensaje explicativo para un icono de la barra de estado es implementar una información sobre herramientas. La información sobre herramientas desaparece al hacer clic en él, pero también puede especificar un valor de tiempo de espera.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488362"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="cee32-104">Cómo implementar la información sobre herramientas para los iconos de la barra de estado</span><span class="sxs-lookup"><span data-stu-id="cee32-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="cee32-105">Una manera no intrusiva de mostrar un mensaje explicativo para un icono de la barra de estado es implementar una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="cee32-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="cee32-106">La información sobre herramientas desaparece al hacer clic en él, pero también puede especificar un valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="cee32-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cee32-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="cee32-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cee32-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="cee32-108">Technologies</span></span>

-   [<span data-ttu-id="cee32-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="cee32-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cee32-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cee32-110">Prerequisites</span></span>

-   <span data-ttu-id="cee32-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="cee32-111">C/C++</span></span>
-   <span data-ttu-id="cee32-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="cee32-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cee32-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cee32-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="cee32-114">Implementar información sobre herramientas para los iconos de la barra de estado</span><span class="sxs-lookup"><span data-stu-id="cee32-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="cee32-115">En el fragmento de código siguiente se muestra cómo agregar una información sobre herramientas de globo a un icono de la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="cee32-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="cee32-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cee32-116">Remarks</span></span>

<span data-ttu-id="cee32-117">Para obtener una explicación detallada de la barra de estado, consulte [la barra de tareas](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="cee32-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="cee32-118">Para mostrar una información sobre herramientas de globo, debe establecer la \_ marca de información de NSI en la estructura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) y usar los miembros **szInfo** y **uTimeout** para especificar el texto de la información sobre herramientas y la duración del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="cee32-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cee32-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cee32-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee32-120">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="cee32-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 