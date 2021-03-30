---
title: Apéndice B compatibilidad del administrador de cuadros de diálogo estándar
description: Microsoft Active Accessibility proporciona compatibilidad completa para los controles de cuadro de diálogo del administrador de cuadros de diálogo estándar (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776404"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="aa36d-103">Apéndice B: compatibilidad con el administrador de cuadros de diálogo estándar</span><span class="sxs-lookup"><span data-stu-id="aa36d-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="aa36d-104">Microsoft Active Accessibility proporciona compatibilidad completa para los controles de cuadro de diálogo del administrador de cuadros de diálogo estándar (SDM).</span><span class="sxs-lookup"><span data-stu-id="aa36d-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="aa36d-105">SDM es una biblioteca de código de Microsoft interna que proporciona a las aplicaciones de Microsoft un grado de independencia de las diferencias entre los sistemas operativos Macintosh y Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa36d-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="aa36d-106">SDM se usa principalmente para cuadros de diálogo de Microsoft Excel y Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="aa36d-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="aa36d-107">SDM presenta problemas para las ayudas de accesibilidad porque utiliza implementaciones no estándar de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="aa36d-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="aa36d-108">Por ejemplo, los botones del cuadro de diálogo SDM no utilizan los identificadores de ventana del mismo modo que los elementos de la interfaz de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="aa36d-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="aa36d-109">No se pueden enviar mensajes a botones y botones no se incluyen en la lista de ventanas.</span><span class="sxs-lookup"><span data-stu-id="aa36d-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="aa36d-110">Una aplicación que usa SDM se comunica con el control a través de una interfaz privada.</span><span class="sxs-lookup"><span data-stu-id="aa36d-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="aa36d-111">En la ilustración siguiente se muestra un cuadro de diálogo de ejemplo de Word.</span><span class="sxs-lookup"><span data-stu-id="aa36d-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="aa36d-112">Aunque parece un cuadro de diálogo normal de Windows que usa el control de pestañas, en realidad es un cuadro de diálogo de SDM.</span><span class="sxs-lookup"><span data-stu-id="aa36d-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![captura de pantalla del cuadro de diálogo Opciones con la pestaña vista seleccionada](images/dialog.gif)

 

 




