---
description: TAPI modela los botones y las lámparas de un teléfono como pares de luces de botón.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Botones de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812482"
---
# <a name="phone-buttons"></a><span data-ttu-id="c8afb-103">Botones de teléfono</span><span class="sxs-lookup"><span data-stu-id="c8afb-103">Phone Buttons</span></span>

<span data-ttu-id="c8afb-104">TAPI modela los botones y las lámparas de un teléfono como pares de luces de botón.</span><span class="sxs-lookup"><span data-stu-id="c8afb-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="c8afb-105">Un botón sin luz junto a él o una lámpara sin botón se especifica mediante un indicador "ficticio" para el botón o lámpara que falta.</span><span class="sxs-lookup"><span data-stu-id="c8afb-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="c8afb-106">Un botón con varias lámparas se modela con varios pares de luz de botón.</span><span class="sxs-lookup"><span data-stu-id="c8afb-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="c8afb-107">La información asociada a un botón de teléfono se puede establecer y recuperar.</span><span class="sxs-lookup"><span data-stu-id="c8afb-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="c8afb-108">Cuando se presiona un botón, se envía un mensaje de [**\_ botón de teléfono**](phone-button.md) a la función de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8afb-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="c8afb-109">Los parámetros de este mensaje son un identificador del dispositivo telefónico y el identificador de la lámpara de botón del botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="c8afb-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="c8afb-110">A los botones del teclado numérico ' 0 ' a ' 9 ', ' \* ' y ' \# ' se les asignan los identificadores de luz de botón fijos del 0 al 11.</span><span class="sxs-lookup"><span data-stu-id="c8afb-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="c8afb-111">Las funciones asociadas a los botones son [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), que establece la información asociada a un botón en un dispositivo telefónico y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), que devuelve información asociada a un botón en un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="c8afb-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="c8afb-112">El mensaje del botón del teléfono \_ se envía a una aplicación cuando se presiona un botón del teléfono.</span><span class="sxs-lookup"><span data-stu-id="c8afb-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="c8afb-113">La información asociada a un botón no tiene ningún significado semántico en lo que se refiere a TAPI.</span><span class="sxs-lookup"><span data-stu-id="c8afb-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="c8afb-114">Resulta útil para aplicaciones específicas del dispositivo que entienden el significado de esta información para un dispositivo telefónico determinado, o para que se muestre al usuario, como la ayuda en línea.</span><span class="sxs-lookup"><span data-stu-id="c8afb-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



