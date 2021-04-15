---
description: Trabajar con menús de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Trabajar con menús de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689594"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="a2f00-103">Trabajar con menús de DVD</span><span class="sxs-lookup"><span data-stu-id="a2f00-103">Working With DVD Menus</span></span>

<span data-ttu-id="a2f00-104">El navegador de DVD puede mostrar un menú cuando el usuario activa un botón o cuando el navegador entra en el primer dominio de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a2f00-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="a2f00-105">Para mostrar un menú mediante programación, llame al método [**IDvdControl2:: showmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .</span><span class="sxs-lookup"><span data-stu-id="a2f00-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="a2f00-106">Hay varias maneras de seleccionar botones de menú mediante programación:</span><span class="sxs-lookup"><span data-stu-id="a2f00-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="a2f00-107">Para seleccionar un botón por número, llame a [**IDvdControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="a2f00-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="a2f00-108">Los botones se numeran del 1 al 36.</span><span class="sxs-lookup"><span data-stu-id="a2f00-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="a2f00-109">El método [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) devuelve el número de botones disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2f00-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="a2f00-110">Para seleccionar un botón relativo a la posición del botón seleccionado actualmente, llame a [**IDvdControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="a2f00-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="a2f00-111">Puede seleccionar un botón en la dirección arriba, abajo, izquierda o derecha.</span><span class="sxs-lookup"><span data-stu-id="a2f00-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="a2f00-112">Para seleccionar un botón por sus coordenadas dentro de la ventana, llame a [**IDvdControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="a2f00-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="a2f00-113">Este método toma las coordenadas (x, y) relativas al área cliente de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a2f00-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="a2f00-114">(Para el modo sin ventanas, esta es la ventana de la aplicación). Si no hay ningún botón en esa ubicación, el método devuelve el \_ botón VFW E \_ DVD \_ no \_ .</span><span class="sxs-lookup"><span data-stu-id="a2f00-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="a2f00-115">Además, hay varias maneras de activar un botón:</span><span class="sxs-lookup"><span data-stu-id="a2f00-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="a2f00-116">Para activar un botón por número, llame a [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span><span class="sxs-lookup"><span data-stu-id="a2f00-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="a2f00-117">Para activar un botón por sus coordenadas, llame a [**IDvdControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span><span class="sxs-lookup"><span data-stu-id="a2f00-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="a2f00-118">Para activar el botón que está seleccionado actualmente, llame a [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="a2f00-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="a2f00-119">Si no se selecciona ningún botón, el método devuelve \_ el \_ botón VFW E DVD \_ no \_ .</span><span class="sxs-lookup"><span data-stu-id="a2f00-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="a2f00-120">Tenga en cuenta que la selección de un botón simplemente resalta los bordes.</span><span class="sxs-lookup"><span data-stu-id="a2f00-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="a2f00-121">Para que se desencadene el comando asociado, se debe activar el botón.</span><span class="sxs-lookup"><span data-stu-id="a2f00-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="a2f00-122">La activación de un botón mediante programación se puede realizar de varias maneras, pero el botón siempre debe estar seleccionado antes de que se pueda activar.</span><span class="sxs-lookup"><span data-stu-id="a2f00-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f00-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2f00-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f00-124">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="a2f00-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



