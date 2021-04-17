---
description: Microsoft telefonía modela los botones y las lámparas de un teléfono como pares de luces de botón.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Botones (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677621"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="01f74-103">Botones (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="01f74-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="01f74-104">Microsoft telefonía modela los botones y las lámparas de un teléfono como pares de luces de botón.</span><span class="sxs-lookup"><span data-stu-id="01f74-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="01f74-105">Un botón sin luz junto a él o una lámpara sin botón se especifica mediante un indicador ficticio para el botón o lámpara que falta.</span><span class="sxs-lookup"><span data-stu-id="01f74-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="01f74-106">Un botón con varias lámparas se modela con varios pares de luz de botón.</span><span class="sxs-lookup"><span data-stu-id="01f74-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="01f74-107">La información asociada a un botón de teléfono se puede establecer y recuperar.</span><span class="sxs-lookup"><span data-stu-id="01f74-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="01f74-108">Cuando se presiona un botón, el proveedor de servicios envía un mensaje de [**\_ botón de teléfono**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) a la función de devolución de llamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="01f74-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="01f74-109">Los parámetros de este mensaje son un identificador del dispositivo telefónico y el identificador de botón o lámpara del botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="01f74-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="01f74-110">Al botón del teclado ' 0 ' a ' 9 ', ' \* ' y ' \# ' se les asignan los identificadores de botón/lámpara fijos del 0 al 11.</span><span class="sxs-lookup"><span data-stu-id="01f74-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="01f74-111">La función [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) establece la información asociada a un botón en un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="01f74-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="01f74-112">[**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) devuelve información asociada a un botón en un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="01f74-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="01f74-113">El proveedor de servicios envía un \_ mensaje de botón de teléfono a la función de devolución de llamada TAPI cuando se presiona un botón del teléfono.</span><span class="sxs-lookup"><span data-stu-id="01f74-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="01f74-114">La información asociada a un botón no lleva ningún significado semántico en lo que se refiere a TSPI.</span><span class="sxs-lookup"><span data-stu-id="01f74-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="01f74-115">Resulta útil para aplicaciones específicas del dispositivo que interpretan esta información para un dispositivo telefónico determinado, o para que se muestre al usuario, como en el sistema de ayuda de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="01f74-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
