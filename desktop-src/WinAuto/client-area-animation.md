---
title: Parámetro de animación del área de cliente
description: La marca de animación del área de cliente indica si el usuario desea deshabilitar las animaciones en elementos de la interfaz de usuario.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271362"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="c380e-103">Parámetro de animación del área de cliente</span><span class="sxs-lookup"><span data-stu-id="c380e-103">Client area animation parameter</span></span>

<span data-ttu-id="c380e-104">El parámetro de animación del área de cliente indica si el usuario desea deshabilitar las animaciones en elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c380e-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="c380e-105">La visualización de características como el parpadeo, el parpadeo, el parpadeo y el traslado de contenido pueden provocar ataques a los usuarios con una epilepsia sensible a la fotografía.</span><span class="sxs-lookup"><span data-stu-id="c380e-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="c380e-106">Este parámetro permite habilitar o deshabilitar todas las animaciones de este tipo.</span><span class="sxs-lookup"><span data-stu-id="c380e-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="c380e-107">Las aplicaciones usan las marcas **SPI \_ GETCLIENTAREAANIMATION** y **SPI \_ SETCLIENTAREAANIMATION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para activar o desactivar las animaciones del área de cliente.</span><span class="sxs-lookup"><span data-stu-id="c380e-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 