---
title: Entrada del mouse (introducción a Win32 y C++)
description: Entrada del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676531"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="be389-103">Entrada del mouse (introducción a Win32 y C++)</span><span class="sxs-lookup"><span data-stu-id="be389-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="be389-104">Windows admite ratones con hasta cinco botones: izquierda, central y derecha, además de dos botones adicionales denominados XBUTTON1 y XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="be389-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![Ilustración que muestra los botones izquierdo (1), derecho (2), medio (3) y xbutton1 (4).](images/mouse.png)

<span data-ttu-id="be389-106">La mayoría de los ratones de Windows tienen al menos los botones izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="be389-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="be389-107">El botón primario del mouse se usa para señalar, seleccionar, arrastrar, etc.</span><span class="sxs-lookup"><span data-stu-id="be389-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="be389-108">El botón secundario del mouse normalmente muestra un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="be389-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="be389-109">Algunos ratones tienen una rueda de desplazamiento situada entre los botones de la izquierda y la derecha.</span><span class="sxs-lookup"><span data-stu-id="be389-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="be389-110">Dependiendo del mouse, es posible que también se pueda hacer clic en la rueda de desplazamiento, convirtiéndola en el botón central.</span><span class="sxs-lookup"><span data-stu-id="be389-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="be389-111">Los botones XBUTTON1 y XBUTTON2 se encuentran a menudo en los lados del mouse, cerca de la base.</span><span class="sxs-lookup"><span data-stu-id="be389-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="be389-112">Estos botones adicionales no están presentes en todos los ratones.</span><span class="sxs-lookup"><span data-stu-id="be389-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="be389-113">Si está presente, los botones XBUTTON1 y XBUTTON2 suelen estar asignados a una función de aplicación, como la navegación hacia delante y hacia atrás en un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="be389-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="be389-114">Los usuarios de la mano izquierda suelen encontrar más cómodo intercambiar las funciones de los botones izquierdo y derecho, con el botón derecho como puntero y el botón izquierdo para mostrar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="be389-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="be389-115">Por esta razón, la documentación de la ayuda de Windows usa el botón *primario* términos y el *botón secundario*, que hacen referencia a la función lógica en lugar de a la selección de ubicación física.</span><span class="sxs-lookup"><span data-stu-id="be389-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="be389-116">En el valor predeterminado (mano derecha), el botón izquierdo es el botón primario y el derecho es el botón secundario.</span><span class="sxs-lookup"><span data-stu-id="be389-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="be389-117">Sin embargo, los términos *haga clic con el botón derecho* y haga *clic* en acciones lógicas.</span><span class="sxs-lookup"><span data-stu-id="be389-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="be389-118">*Hacer clic con el botón derecho* significa hacer clic en el botón principal, tanto si el botón está físicamente a la derecha como en el lado izquierdo del mouse.</span><span class="sxs-lookup"><span data-stu-id="be389-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="be389-119">Independientemente de la forma en que el usuario configure el mouse, Windows traduce automáticamente los mensajes del mouse para que sean coherentes.</span><span class="sxs-lookup"><span data-stu-id="be389-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="be389-120">El usuario puede intercambiar los botones principal y secundario en medio de usar el programa y no afectará a la forma en que se comporta el programa.</span><span class="sxs-lookup"><span data-stu-id="be389-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="be389-121">En la documentación de MSDN se usa el botón *derecho* y el *botón primario* para hacer referencia al botón *principal* y *secundario* .</span><span class="sxs-lookup"><span data-stu-id="be389-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="be389-122">Esta terminología es coherente con los nombres de los mensajes de ventana para la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="be389-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="be389-123">Solo tiene que recordar que se pueden intercambiar los botones físicos izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="be389-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="be389-124">Siguientes</span><span class="sxs-lookup"><span data-stu-id="be389-124">Next</span></span>

[<span data-ttu-id="be389-125">Responder a clics del mouse</span><span class="sxs-lookup"><span data-stu-id="be389-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




