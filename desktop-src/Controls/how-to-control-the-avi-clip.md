---
title: Cómo controlar el clip AVI
description: En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip Audio-Video intercalado (AVI) asociado.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488596"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="14a63-103">Cómo controlar el clip AVI</span><span class="sxs-lookup"><span data-stu-id="14a63-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="14a63-104">En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip Audio-Video intercalado (AVI) asociado.</span><span class="sxs-lookup"><span data-stu-id="14a63-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="14a63-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="14a63-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="14a63-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="14a63-106">Technologies</span></span>

-   [<span data-ttu-id="14a63-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="14a63-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="14a63-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="14a63-108">Prerequisites</span></span>

-   <span data-ttu-id="14a63-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="14a63-109">C/C++</span></span>
-   <span data-ttu-id="14a63-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="14a63-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="14a63-111">Archivos AVI</span><span class="sxs-lookup"><span data-stu-id="14a63-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="14a63-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="14a63-112">Instructions</span></span>


<span data-ttu-id="14a63-113">Cree una función que toma como parámetros un identificador del control Animation y una marca que indica la acción que se va a realizar en el clip AVI asociado.</span><span class="sxs-lookup"><span data-stu-id="14a63-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="14a63-114">En el siguiente ejemplo de C++, la función llama a una de las tres macros de control de animación ([**animar \_ reproducir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animar \_ detener**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)y [**animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) en función del valor del parámetro *nAcción* .</span><span class="sxs-lookup"><span data-stu-id="14a63-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="14a63-115">El identificador del control de animación que está asociado al clip AVI se pasa a través del parámetro *hwndAnim* .</span><span class="sxs-lookup"><span data-stu-id="14a63-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a><span data-ttu-id="14a63-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14a63-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a63-117">Acerca de los controles de animación</span><span class="sxs-lookup"><span data-stu-id="14a63-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="14a63-118">Referencia de control de animación</span><span class="sxs-lookup"><span data-stu-id="14a63-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="14a63-119">Usar controles de animación</span><span class="sxs-lookup"><span data-stu-id="14a63-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="14a63-120">Animation (control)</span><span class="sxs-lookup"><span data-stu-id="14a63-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




