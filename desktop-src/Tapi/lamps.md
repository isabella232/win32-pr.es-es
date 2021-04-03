---
description: Las luces de un dispositivo telefónico se pueden iluminar en distintos modos de iluminación.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lámparas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083180"
---
# <a name="lamps"></a><span data-ttu-id="35204-103">Lámparas</span><span class="sxs-lookup"><span data-stu-id="35204-103">Lamps</span></span>

<span data-ttu-id="35204-104">Las luces de un dispositivo telefónico se pueden iluminar en distintos modos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="35204-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="35204-105">A diferencia de los modelos de timbre, los modos de lámpara son más uniformes en los juegos de teléfono de distintos proveedores.</span><span class="sxs-lookup"><span data-stu-id="35204-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="35204-106">La API define un conjunto común de modos de lámpara.</span><span class="sxs-lookup"><span data-stu-id="35204-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="35204-107">Una lámpara identificada por su identificador de botón de lámpara puede estar iluminada en un modo de lámpara determinado.</span><span class="sxs-lookup"><span data-stu-id="35204-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="35204-108">También se puede consultar una lámpara para el modo de lámpara actual.</span><span class="sxs-lookup"><span data-stu-id="35204-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="35204-109">Las funciones TAPI que se usan para las lámparas son [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que ilumina una lámpara en un dispositivo de teléfono abierto especificado en un modo de iluminación de lámpara determinado y [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que devuelve el modo de lámpara actual de la lámpara especificada.</span><span class="sxs-lookup"><span data-stu-id="35204-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="35204-110">Cuando se cambia una lámpara de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="35204-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="35204-111">Los parámetros de este mensaje proporcionan una indicación del cambio.</span><span class="sxs-lookup"><span data-stu-id="35204-111">Parameters to this message provide an indication of the change.</span></span>

 

 



