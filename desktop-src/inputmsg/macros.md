---
title: Macros
description: En los temas de esta sección se proporcionan las especificaciones de referencia para los mensajes de entrada de puntero y las macros de notificaciones para recuperar información de los parámetros de mensajes de entrada de puntero.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2020
ms.locfileid: "104420146"
---
# <a name="macros"></a><span data-ttu-id="fee66-103">Macros</span><span class="sxs-lookup"><span data-stu-id="fee66-103">Macros</span></span>

<span data-ttu-id="fee66-104">En los temas de esta sección se proporcionan las especificaciones de referencia para [los mensajes de entrada de puntero y](messages-and-notifications-portal.md) las macros de notificaciones para recuperar información de los parámetros de mensajes de entrada de puntero.</span><span class="sxs-lookup"><span data-stu-id="fee66-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fee66-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fee66-105">In this section</span></span>



| <span data-ttu-id="fee66-106">Tema</span><span class="sxs-lookup"><span data-stu-id="fee66-106">Topic</span></span>                                                                                  | <span data-ttu-id="fee66-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fee66-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fee66-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="fee66-109">Recupera el identificador de puntero mediante el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="fee66-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="fee66-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="fee66-111">Comprueba si el mensaje de puntero especificado se considera intencionado en lugar de accidental.</span><span class="sxs-lookup"><span data-stu-id="fee66-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="fee66-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="fee66-113">Comprueba si la entrada de puntero especificada finalizó repentinamente o no era válida, lo que indica que no se completó la interacción.</span><span class="sxs-lookup"><span data-stu-id="fee66-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="fee66-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="fee66-115">Comprueba si el puntero especificado tardó la quinta acción.</span><span class="sxs-lookup"><span data-stu-id="fee66-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="fee66-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="fee66-117">Comprueba si el puntero especificado tomó la primera acción.</span><span class="sxs-lookup"><span data-stu-id="fee66-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="fee66-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="fee66-119">Comprueba si una macro de puntero establece la marca especificada.</span><span class="sxs-lookup"><span data-stu-id="fee66-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="fee66-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="fee66-121">Comprueba si el puntero especificado tardó la cuarta acción.</span><span class="sxs-lookup"><span data-stu-id="fee66-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="fee66-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="fee66-123">Comprueba si el puntero especificado está en el contacto.</span><span class="sxs-lookup"><span data-stu-id="fee66-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="fee66-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="fee66-125">Comprueba si el puntero especificado está dentro del intervalo.</span><span class="sxs-lookup"><span data-stu-id="fee66-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="fee66-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="fee66-127">Comprueba si el puntero especificado es un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="fee66-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="fee66-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="fee66-129">Comprueba si el puntero especificado es el puntero primario.</span><span class="sxs-lookup"><span data-stu-id="fee66-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="fee66-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="fee66-131">Comprueba si el puntero especificado tardó la segunda acción.</span><span class="sxs-lookup"><span data-stu-id="fee66-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="fee66-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="fee66-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="fee66-133">Comprueba si el puntero especificado tardó la tercera acción.</span><span class="sxs-lookup"><span data-stu-id="fee66-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="fee66-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fee66-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee66-135">Referencia de mensajes de entrada de puntero</span><span class="sxs-lookup"><span data-stu-id="fee66-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





