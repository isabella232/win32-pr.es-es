---
description: Introducción al uso de controles sin propiedades de título para Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controles sin propiedades de título
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539436"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="98df6-103">Controles sin propiedades de título</span><span class="sxs-lookup"><span data-stu-id="98df6-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="98df6-104">Cuando un control no tiene su propia propiedad Caption, realice los pasos siguientes para asegurarse de que las ayudas de accesibilidad pueden identificar los controles:</span><span class="sxs-lookup"><span data-stu-id="98df6-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="98df6-105">Cree un control de texto estático con un nombre descriptivo y significativo.</span><span class="sxs-lookup"><span data-stu-id="98df6-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="98df6-106">Coloque la etiqueta estática para que preceda inmediatamente al control al que se hace referencia, en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="98df6-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="98df6-107">Asegúrese de que el texto de la etiqueta termina con dos puntos, por ejemplo, "configuración:"</span><span class="sxs-lookup"><span data-stu-id="98df6-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="98df6-108">Coloca el texto de la etiqueta inmediatamente a la izquierda o delante del control al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="98df6-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="98df6-109">Haga que el texto estático sea invisible si no es adecuado para mostrarlo visualmente.</span><span class="sxs-lookup"><span data-stu-id="98df6-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="98df6-110">Para ello, asigne el atributo adecuado en el script de recursos.</span><span class="sxs-lookup"><span data-stu-id="98df6-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="98df6-111">Esto puede ser adecuado cuando el nombre o la función de un control se proporciona visualmente a través de un control de texto estático, como un gráfico o un botón de radio relacionado.</span><span class="sxs-lookup"><span data-stu-id="98df6-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="98df6-112">El uso correcto de los controles estáticos es la única manera de implementar correctamente las teclas de acceso subrayadas para los controles que no tienen etiquetas intrínsecas.</span><span class="sxs-lookup"><span data-stu-id="98df6-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="98df6-113">Para obtener más información sobre el uso de controles que no tienen propiedades de título, vea la sección [accesibilidad](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="98df6-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
